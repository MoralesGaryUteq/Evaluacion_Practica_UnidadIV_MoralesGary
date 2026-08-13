# Evaluación Práctica — Unidad IV — Ingeniería de Requisitos (ISR-401)

Universidad Técnica Estatal de Quevedo · Facultad de Ciencias de la Ingeniería · Carrera de Ingeniería de Software

**Caso práctico:** Sistema de Reserva de Citas Médicas
**Estudiante:** Morales Sánchez Gary Alejandro — CI: 1251154173 — gmoraless2@uteq.edu.ec
**Curso/Paralelo:** Cuarto semestre, Paralelo "B"
**Docente:** Ing. Gleiston Guerrero, Mg.
**Fecha:** 12/08/2026

**Repositorio:** https://github.com/MoralesGaryUteq/Evaluacion_Practica_UnidadIV_MoralesGary

---

## 1. Archivo principal

`MoralesGary_Evaluacion_U4.tex`

## 2. Estructura del repositorio

```
.
├── MoralesGary_Evaluacion_U4.tex   # Archivo principal (documento fuente)
├── MoralesGary_Evaluacion_U4.pdf   # PDF compilado
├── referencias.bib                    # Base bibliográfica (BibTeX)
├── README.md                          # Este archivo
└── figuras/
    ├── Resumen_Evaluacion_LMS.png     # Captura: resumen del cuestionario SGA
    ├── Revision_intento_lms.png       # Captura: evaluación/intento SGA
    ├── Diagramadeclases.png           # P1 — Diagrama de clases UML
    ├── diagramadeactividades.png      # P2 — Diagrama de actividades UML
    ├── diagramamaquinadeestado.png    # P3 — Máquina de estados UML
    └── revision_pg-1.jpg … revision_pg-11.jpg   # Anexo: revisión del intento
```

Los nombres de archivo de las figuras deben respetarse tal cual (sin tildes ni espacios), porque están referenciados literalmente en el `.tex`.

## 3. Compilador

`pdflatex` (TeX Live 2023 o superior, o MiKTeX actualizado) más `bibtex` para la bibliografía.

## 4. Orden exacto de comandos

Desde la raíz del repositorio, con el archivo principal sin extensión:

```bash
pdflatex MoralesGary_Evaluacion_U4
bibtex   MoralesGary_Evaluacion_U4
pdflatex MoralesGary_Evaluacion_U4
pdflatex MoralesGary_Evaluacion_U4
```

Las dos últimas pasadas son necesarias para resolver referencias cruzadas, citas y numeración de tablas y figuras.

Alternativa equivalente en un solo comando:

```bash
latexmk -pdf MoralesGary_Evaluacion_U4.tex
```

## 5. Reproducción desde cero

```bash
git clone https://github.com/MoralesGaryUteq/Evaluacion_Practica_UnidadIV_MoralesGary.git
cd Evaluacion_Practica_UnidadIV_MoralesGary
pdflatex MoralesGary_Evaluacion_U4
bibtex   MoralesGary_Evaluacion_U4
pdflatex MoralesGary_Evaluacion_U4
pdflatex MoralesGary_Evaluacion_U4
```

El resultado es `MoralesGary_Evaluacion_U4.pdf` en la misma carpeta.

## 6. Dependencias (paquetes LaTeX)

Todos pertenecen a la distribución estándar; en TeX Live se cubren con `texlive-latex-recommended`, `texlive-latex-extra` y `texlive-fonts-recommended`.

| Paquete | Uso en el documento |
|---|---|
| `inputenc` (utf8), `fontenc` (T1) | Codificación de entrada y salida de fuentes |
| `helvet`, `textcomp` | Tipografía sans-serif institucional y símbolos |
| `geometry` | Márgenes A4 y altura de encabezado |
| `amsmath`, `amssymb` | Notación matemática |
| `graphicx` | Inclusión de figuras |
| `xcolor` (opciones `table`, `dvipsnames`) | Paleta institucional y color de filas |
| `array`, `tabularx`, `multirow`, `colortbl`, `booktabs` | Construcción de tablas |
| `enumitem` | Ajuste de listas |
| `microtype` | Ajuste tipográfico fino |
| `parskip` | Separación entre párrafos |
| `titlesec` | Formato de títulos de sección |
| `fancyhdr` | Encabezados y pies de página |
| `caption` | Formato de leyendas |
| `pdflscape` | Página apaisada de la rúbrica |
| `natbib` (opciones `numbers`, `sort&compress`) | Citas y bibliografía |
| `hyperref` | Enlaces y metadatos del PDF |
| `tcolorbox` (opciones `skins`, `breakable`) | Cajas de concepto, criterios de piso y tareas |
| `float` | Ubicación fija de figuras (`[H]`) |

Instalación de dependencias en Debian/Ubuntu:

```bash
sudo apt install texlive-latex-base texlive-latex-recommended \
                 texlive-latex-extra texlive-fonts-recommended \
                 texlive-bibtex-extra biber latexmk
```

## 7. Contenido evaluado

| Tarea | Producto |
|---|---|
| P1 | Diagrama de clases UML del dominio |
| P2 | Diagrama de actividades UML del proceso "Agendar cita" |
| P3 | Máquina de estados UML del ciclo de vida de la Cita |
| P4 | Tabla de verificación cruzada, defectos DEF-01 y DEF-02 con su corrección |
| P5 | 4 requisitos (RF-01, RF-02, RNF-01, RNF-02) con métricas ISO/IEC 25010:2023 y esquema de atributos |
| P6 | Priorización MoSCoW justificada |
| P7 | Lista de comprobación ISO/IEC/IEEE 29148, defectos DF-01…DF-05 y retrabajo |
| P8 | No realizado |
| P9 | No realizado |
| P10 | No realizado |

## 8. Notas

- El documento incluye la carátula con la URL del repositorio en una sola línea y las capturas del resumen y de la evaluación del cuestionario rendido en el SGA (criterios de piso).
- Si `bibtex` reporta que no encuentra entradas, verificar que `referencias.bib` esté en la raíz, junto al archivo principal.
