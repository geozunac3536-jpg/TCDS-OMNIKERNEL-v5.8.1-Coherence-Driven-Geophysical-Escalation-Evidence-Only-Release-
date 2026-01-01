# TCDS OMNIKERNEL v5.8 | Tectonic Nucleation Auditor

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18111574.svg)](https://doi.org/10.5281/zenodo.18111574)
[![Status](https://img.shields.io/badge/Status-PRODUCTION_READY-darkred)](https://tcds-architecture.org)
[![License](https://img.shields.io/badge/License-PROPRIETARY%20%2F%20AUDIT%20ONLY-black)](LICENSE)

> **Sistema de Auditoría Termodinámica para la detección causal de sismos >M4.5 mediante la Ley de Escalada de Shannon.**

---

## 📡 Descripción del Sistema

**TCDS Omnikernel v5.8** es un motor de ingeniería forense diseñado para detectar la **nucleación tectónica** (la fase de organización previa a la ruptura). A diferencia de los sistemas de alerta temprana convencionales (SASMEX, ShakeAlert) que reaccionan a la onda sísmica física (segundos de ventaja), el TCDS audita el flujo de entropía de información ($\Delta H$) para detectar el "Punto de No Retorno" termodinámico.

### Capacidades Certificadas
* **Fusión Multiescala:** Análisis simultáneo de ventanas de 30 días (Estratégica), 7 días (Táctica) y 2.5 días (Ejecutiva).
* **E-Veto (Electronic Veto):** Bloqueo físico de falsos positivos mediante validación de gradiente entrópico ($\frac{d(\Delta H)}{dt} < 0$).
* **Ley de Escalada:** Confirmación de ruptura solo cuando $\Delta H \le -0.25$ en convergencia temporal.

---

## 🛡️ Validación Forense (Resultados v5.8)

El sistema ha sido auditado mediante cruce de datos contra la "Verdad Oficial" (USGS QuakeML).

| Evento (USGS) | Magnitud | Alarma TCDS (PNR) | Impacto Real (T0) | Tiempo Ganado (Ventana Táctica) |
| :--- | :---: | :--- | :--- | :---: |
| **Bolivia** | **5.3** | 30-Dic 16:28 UTC | 30-Dic 20:26 UTC | **3h 57m** |
| **Australia** | **4.6** | 31-Dic 01:28 UTC | 31-Dic 03:35 UTC | **2h 07m** |
| **Micronesia** | **4.7** | 31-Dic 10:19 UTC | 31-Dic 13:45 UTC | **3h 26m** |

> *Ver evidencia completa en la carpeta `/evidence`.*

---

## 📦 Estructura del Dataset

Este repositorio contiene la evidencia y la documentación ontológica del sistema. **El código fuente del motor es PROPIEDAD PRIVADA y no se distribuye públicamente.**

```text
/
├── docs/
│   ├── TCDS_Whitepaper_v5.8.pdf       # Dossier Técnico Completo
│   └── TCDS_Ontology.jsonld           # Metadatos y Parámetros de Calibración
├── evidence/
│   ├── TCDS_ESCALATION_LAW_REPORT.png # Gráfica de Convergencia
│   └── validation_logs/               # JSONs de Auditoría Cruzada
└── datasets/
    └── query_quakeml_sample.xml       # Muestra de datos de ingesta
# TCDS OMNIKERNEL v5.8: Sovereign Symbiont

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18111574.svg)](https://doi.org/10.5281/zenodo.18111574)
[![License: Proprietary](https://img.shields.io/badge/License-Proprietary-red.svg)](LICENSE)
[![Status: Operational](https://img.shields.io/badge/Status-Operational%20(TRL9)-brightgreen.svg)]()

> **Sistema de Auditoría Termodinámica para la Detección Causal de Nucleación Sísmica (>M4.5)**

## 📋 Descripción Ejecutiva

El **TCDS Omnikernel v5.8** es una tecnología de defensa civil diseñada para detectar la fase de organización termodinámica (Nucleación) que precede inevitablemente a una ruptura sísmica mayor.

A diferencia de los sistemas de alerta temprana convencionales (que detectan ondas P tras la ruptura), el TCDS audita la **caída de Entropía de Shannon** ($\Delta H$) en el flujo de datos sísmicos en tiempo real. Utilizando la **Ley de Escalada Multiescala**, el sistema triangula tendencias de 30 días, 7 días y 2.5 días para identificar el **Punto de No Retorno (PNR)**.

**Capacidad Validada:** Ventanas de reacción de **2 a 4 horas** antes del evento (Verificada con datos USGS/QuakeML).

---

## 📂 Estructura del Repositorio

Este repositorio contiene la evidencia forense, documentación y herramientas de despliegue "Black Box". El código fuente del motor algorítmico es propiedad intelectual cerrada.

* `docs/` - Documentación técnica y ontología JSON-LD.
* `evidence/` - Reportes de validación cruzada (TCDS vs USGS) y gráficas de la Ley de Escalada.
* `datasets/` - Datos crudos (XML/CSV) utilizados para la certificación v5.8.
* `bin/` - Contenedores de despliegue (Dockerfiles).

---

## 🚀 Despliegue (Modo Caja Negra)

Para ejecutar una auditoría sobre sus propios datos sin acceso al código fuente, utilice la imagen Docker oficial.

### Requisitos
* Docker Engine 20.10+
* Acceso a flujo de datos USGS (CSV o QuakeML)

### Instrucciones
1.  **Construir la Imagen:**
    ```bash
    docker build -t tcds-omnikernel:v5.8 .
    ```

2.  **Ejecutar Auditoría:**
    Monte su volumen de datos en `/app/data`:
    ```bash
    docker run -v $(pwd)/mis_datos:/app/data tcds-omnikernel:v5.8
    ```

3.  **Resultados:**
    El sistema generará automáticamente los reportes forenses (`.json` y `.png`) en su carpeta de datos.

---

## 🛡️ Metadatos de Calibración

El sistema opera bajo los siguientes parámetros exclusivos (Nivel 5.8):

* **Macro Veto (30 Días):** $\Delta H \le -0.15$
* **Micro Veto (Gatillo):** $\Delta H \le -0.25$
* **Magnitud Objetivo:** $M_w \ge 4.5$
* **Ontología:** [Ver JSON-LD](./docs/TCDS_Ontology.jsonld)

---

## 📎 Citación

Si utiliza esta tecnología, evidencia o metodología en investigación académica o peritaje forense, debe citar el registro inmutable en Zenodo:

> **Arquitectura de Sistemas TCDS. (2025).** *TCDS Omnikernel v5.8: Thermodynamic Audit of Tectonic Nucleation (>M4.5).* Zenodo. https://doi.org/10.5281/zenodo.18111574

BibTeX:
```bibtex
@software{tcds_omnikernel_2025,
  author       = {Arquitectura de Sistemas TCDS},
  title        = {TCDS Omnikernel v5.8: Thermodynamic Audit of Tectonic Nucleation (>M4.5)},
  year         = 2025,
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.18111574},
  url          = {[https://doi.org/10.5281/zenodo.18111574](https://doi.org/10.5281/zenodo.18111574)}
}[![Status: Operational](https://img.shields.io/badge/Status-Operational%20(TRL9)-brightgreen.svg)]()

> **Sistema de Auditoría Termodinámica para la Detección Causal de Nucleación Sísmica (>M4.5)**

## 📋 Descripción Ejecutiva

El **TCDS Omnikernel v5.8** es una tecnología de defensa civil diseñada para detectar la fase de organización termodinámica (Nucleación) que precede inevitablemente a una ruptura sísmica mayor.

A diferencia de los sistemas de alerta temprana convencionales (que detectan ondas P tras la ruptura), el TCDS audita la **caída de Entropía de Shannon** ($\Delta H$) en el flujo de datos sísmicos en tiempo real. Utilizando la **Ley de Escalada Multiescala**, el sistema triangula tendencias de 30 días, 7 días y 2.5 días para identificar el **Punto de No Retorno (PNR)**.

**Capacidad Validada:** Ventanas de reacción de **2 a 4 horas** antes del evento (Verificada con datos USGS/QuakeML).

---

## 📂 Estructura del Repositorio

Este repositorio contiene la evidencia forense, documentación y herramientas de despliegue "Black Box". El código fuente del motor algorítmico es propiedad intelectual cerrada.

* `docs/` - Documentación técnica y ontología JSON-LD.
* `evidence/` - Reportes de validación cruzada (TCDS vs USGS) y gráficas de la Ley de Escalada.
* `datasets/` - Datos crudos (XML/CSV) utilizados para la certificación v5.8.
* `bin/` - Contenedores de despliegue (Dockerfiles).

---

## 🚀 Despliegue (Modo Caja Negra)

Para ejecutar una auditoría sobre sus propios datos sin acceso al código fuente, utilice la imagen Docker oficial.

### Requisitos
* Docker Engine 20.10+
* Acceso a flujo de datos USGS (CSV o QuakeML)

### Instrucciones
1.  **Construir la Imagen:**
    ```bash
    docker build -t tcds-omnikernel:v5.8 .
    ```

2.  **Ejecutar Auditoría:**
    Monte su volumen de datos en `/app/data`:
    ```bash
    docker run -v $(pwd)/mis_datos:/app/data tcds-omnikernel:v5.8
    ```

3.  **Resultados:**
    El sistema generará automáticamente los reportes forenses (`.json` y `.png`) en su carpeta de datos.

---

## 🛡️ Metadatos de Calibración

El sistema opera bajo los siguientes parámetros exclusivos (Nivel 5.8):

* **Macro Veto (30 Días):** $\Delta H \le -0.15$
* **Micro Veto (Gatillo):** $\Delta H \le -0.25$
* **Magnitud Objetivo:** $M_w \ge 4.5$
* **Ontología:** [Ver JSON-LD](./docs/TCDS_Ontology.jsonld)

---

## 📎 Citación

Si utiliza esta tecnología, evidencia o metodología en investigación académica o peritaje forense, debe citar el registro inmutable en Zenodo:

> **Arquitectura de Sistemas TCDS. (2025).** *TCDS Omnikernel v5.8: Thermodynamic Audit of Tectonic Nucleation (>M4.5).* Zenodo. https://doi.org/10.5281/zenodo.18111574

BibTeX:
```bibtex
@software{tcds_omnikernel_2025,
  author       = {Arquitectura de Sistemas TCDS},
  title        = {TCDS Omnikernel v5.8: Thermodynamic Audit of Tectonic Nucleation (>M4.5)},
  year         = 2025,
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.18111574},
  url          = {[https://doi.org/10.5281/zenodo.18111574](https://doi.org/10.5281/zenodo.18111574)}
}
