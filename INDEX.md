# MANIFIESTO DE ENTREGA: TCDS OMNIKERNEL v5.8 (Evidence Release)

**ID de Entrega:** `TCDS-REL-5.8.1`
**DOI (Zenodo):** `10.5281/zenodo.18111574`
**Fecha de Congelación:** 31-Diciembre-2025

Este paquete contiene **documentación**, **datasets** y **evidencia forense** asociada a la corrida v5.8.
> Nota: **No incluye el núcleo ejecutable** (black‑box / core propietario). Este release es “evidence‑only”.

---

## 1) Documentación (`/docs`)
| Archivo | Descripción | Acceso |
| :--- | :--- | :--- |
| `TCDS_Whitepaper_v5_8.pdf` | Dossier técnico (metodología, criterios, alcance). | Público |
| `TCDS_Ontology.jsonld` | Ontología/metadata semántica del paquete. | Público |

## 2) Evidencia Forense (`/evidence`)
| Archivo | Descripción | Acceso |
| :--- | :--- | :--- |
| `TCDS_ESCALATION_LAW_GEO_REPORT.json` | Reporte estructurado (geo/ley/escalamiento). | Público |
| `TCDS_ESCALATION_LAW_REPORT.png` | Render/figura del reporte. | Público |
| `MANIFEST.txt` | Manifiesto interno (hashes parciales + referencia DOI). | Público |

## 3) Datasets (`/datasets`)
| Archivo | Descripción |
| :--- | :--- |
| `30_day.csv` | Ventana 30 días (macro). |
| `7_day.csv` | Ventana 7 días (táctica). |
| `2.5_day.csv` | Ventana 2.5 días (evento-cero / micro). |
| `query.quakeml.xml` | Catálogo QuakeML principal (consulta). |
| `quakeml.xml` | Catálogo QuakeML (base). |
| `quakeml_1.xml` | Catálogo QuakeML (duplicado/versionado). |
| `quakeml_2.xml` | Catálogo QuakeML (duplicado/versionado). |

## 4) Contenedor de Transporte (`/bin`)
| Archivo | Propósito |
| :--- | :--- |
| `Dockerfile` | Contenedor **evidence-only** (empaqueta docs/datasets/evidence; no ejecuta el core). |

## 5) Integridad criptográfica
- `CHECKSUMS.sha256` (raíz) contiene SHA‑256 de **todos los archivos** de este release.

---
**Regla de lectura rápida:** si el contenido del `INDEX.md` no coincide con el árbol del ZIP, el ZIP está corrupto o no corresponde a la versión indicada.
