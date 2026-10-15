# Informe Laboratorio 3 — Seguridad de contraseñas en Mega

Informe del Laboratorio 3 (Sección 2), escrito en LaTeX. Analiza cómo **Mega** (`mega.nz`) procesa las contraseñas desde el navegador, qué mecanismos criptográficos usa en el registro y en el inicio de sesión, y si un valor de autenticación derivado puede reutilizarse sin conocer la contraseña original (*Pass the Hash*).

**Autor:** Francisco Polanco — francisco.polanco@mail.udp.cl
**Fecha:** Octubre de 2026

## Contenido del informe

El desarrollo sigue los criterios de la rúbrica:

1. Identificación del algoritmo de hash usado al **registrarse** en el sitio.
2. Identificación del algoritmo de hash usado al **iniciar sesión**.
3. Generación del hash de la contraseña desde la **consola del navegador**.
4. Intercepción del tráfico de login con **BurpSuite**.
5. Intento de login reemplazando una contraseña incorrecta por el hash obtenido (*Pass the Hash*).
6. Políticas de privacidad y seguridad relacionadas con las contraseñas.
7. Cuatro conclusiones sobre la seguridad de la implementación observada.

## Estructura del repositorio

```
.
├── informe.tex      # Documento principal
├── figuras/         # Capturas usadas en el informe (fig01 … fig16 y diagramas de código)
└── README.md
```

En `figuras/`, los archivos terminados en `_orig` son las capturas originales y los terminados en `_recorte` son las versiones recortadas.

## Cómo compilar

Requiere una distribución de LaTeX (TeX Live, MiKTeX o similar) con los paquetes `graphicx`, `subcaption`, `babel` (spanish), `xcolor`, `float`, `hyperref` y `listings`.

```bash
pdflatex informe.tex
pdflatex informe.tex   # segunda pasada para generar el índice y las referencias
```

También se puede compilar en [Overleaf](https://www.overleaf.com/) subiendo el repositorio como proyecto y dejando `informe.tex` como documento principal.

## Nota de seguridad

Las pruebas se hicieron con una cuenta creada exclusivamente para el laboratorio, y la contraseña utilizada fue reemplazada al terminar la actividad, por lo que los valores capturados en las figuras ya no corresponden a una credencial vigente.

## Contexto académico

Trabajo realizado para un curso de la Universidad Diego Portales (UDP). Se publica con fines académicos y educativos.
