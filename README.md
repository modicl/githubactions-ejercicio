# GitHub Actions - Ejercicio ETL

Proyecto de ETL automatizado que extrae datos de la API de Coderhouse y los carga en Snowflake usando GitHub Actions.

## Descripción

Este proyecto automatiza el proceso de:
1. Extracción de datos desde la API de Coderhouse
2. Carga de datos en Snowflake (tablas: usuarios, reseñas, cursos, inscripciones)

## Estructura del Proyecto

```
├── scripts/
│   ├── extract.py      # Script de extracción de datos
│   ├── load.py         # Script de carga a Snowflake
│   └── query.sql       # Consultas SQL
├── requirements.txt    # Dependencias del proyecto
└── README.md
```

## Requisitos

- Python 3.x
- Cuenta de Snowflake
- Credenciales configuradas como secrets en GitHub

## Variables de Entorno

- `SNOWSQL_USER`: Usuario de Snowflake
- `SNOWSQL_PWD`: Contraseña de Snowflake
- `SNOWSQL_ACCOUNT`: Cuenta de Snowflake

## Instalación Local

```bash
pip install -r requirements.txt
```

## Uso

### Extracción de datos
```bash
python scripts/extract.py
```

### Carga a Snowflake
```bash
python scripts/load.py
```

## Automatización

El proyecto utiliza GitHub Actions para ejecutar automáticamente el pipeline ETL.
Repo con GitHub Actions
