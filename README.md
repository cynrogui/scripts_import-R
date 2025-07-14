# scripts_import-R
# ----------------------------------------------------------
# Módulo 1 Wrangling: Ingesta y Organización de Datos
# Actividad transversal 1
# ----------------------------------------------------------

# Instalación de paquetes 
install.packages("readr")
install.packages("readxl")
install.packages("here")
install.packages("dplyr")
install.packages("rvest")

# Cargar librerías necesarias
library(readr)
library(readxl)
library(here)
library(dplyr)
library(rvest)

# 1. Crear un proyecto con estructura rofesional con carpeta data que contenga 
# raw y processed, crear carpeta scripts y crear carpeta outputs

# 2. Ingesta de datos

# 2.1. Lectura de archio plano CSV

datos_csv <- read_csv(here("data", "raw", "datos.csv"))


# 2.2. Lectura directa desde la página web https://snif.cnf.gob.mx/incendios/

datos_web <- read_html("https://snif.cnf.gob.mx/incendios/datos.html")
