# Pipeline de Reducción Espectral: Metalicidad y Evolución Química de Galaxias (SDSS)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/TU_USUARIO/TU_REPOSITORIO/blob/main/Proyecto3_Metalicidad_SDSS.ipynb)
[![Astropy](https://img.shields.io/badge/powered%20by-AstroPy-orange.svg?style=flat)](http://www.astropy.org/)

Este repositorio contiene un pipeline automático desarrollado en Python para la extracción, reducción espectral y análisis químico de galaxias con formación estelar a partir del Sloan Digital Sky Survey (SDSS DR18).

## Ejecución
Puedes ejecutar el proyecto completo en la nube con un solo clic. Presione el botón Open in Colab que aparece arriba en este README (recuerde actualizar el enlace con su usuario de GitHub).

## Características del Pipeline
El código realiza de forma secuencial los siguientes procesos físicos:
- Query SQL Remoto: Descarga masiva de datos espectrales y fotométricos de galaxias en el universo local (0.01 < z < 0.1).
- Correcciones Astrofísicas: Corrección cinemática por Redshift, sustracción del continuo local y remoción de extinción por polvo de la Vía Láctea (Mapas SFD + Ley CCM89).
- Ajuste de Líneas: Modelado Gaussiano de perfiles para las líneas H\beta, [OIII]\lambda5007, H\alpha y [NII]\lambda6584.
- Control de Calidad: Filtrado estricto por Relación Señal/Ruido (S/N > 5).
- Física Nebular: Corrección por polvo intrínseco (Decremento de Balmer) y cálculo de abundancia química mediante el calibrador empírico O3N2 (Pettini & Pagel 2004).

## Entregables 
- GAME.ipynb: Notebook reproducible paso a paso listo para Google Colab.
- catalogo_final_entregables.csv: El catálogo físico resultante con los parámetros medidos de las 100 galaxias.
- graficos.png: Gráfico científico de tres paneles que abarca el Diagrama BPT, Histograma de EW(Halpha) y la relación Masa-Metalicidad.


