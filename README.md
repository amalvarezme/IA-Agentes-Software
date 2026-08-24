# IA-Agentes-Software

Deck del seminario **"Principios de IA agéntica para el desarrollo de software"**, del Laboratorio de Inteligencia Artificial de la Universidad Nacional de Colombia sede Manizales.

**Presentación en vivo: https://amalvarezme.github.io/IA-Agentes-Software/**

Autor: A.M Álvarez-Meza, PhD — Seminario de Investigación, UNAL Manizales.

## Qué es

Una presentación estática (HTML + CSS + JS, sin build ni dependencias) de 49 slides organizados en 14 módulos, más una serie de guías de demo en vivo.

## Contenido

| # | Módulo | Tema |
|---|--------|------|
| 1 | IA Agéntica | Marco general |
| 2 | IA → Software | Del chat al sistema |
| 3 | Forward Deployed Engineer | Rol y práctica |
| 4 | SetUp | Preparación del entorno |
| 5 | IA Generativa | Qué es y qué no es un LLM |
| 6 | Context Window | Attention decay y compactación |
| 7 | Chat vs Agente | Tools y capacidad de acción |
| 8 | Evolución del Contexto | AGENTS.md → Skills → sub-agentes |
| 9 | God Agent | Por qué degrada un agente monolítico |
| 10 | SDD Orchestrator | Spec-Driven Development y el DAG de fases |
| 11 | Engram | Memoria persistente entre sesiones |
| 12 | Skills Registry | Progressive disclosure de instrucciones |
| 13 | Stack y Bibliotecas | gentle-ai y ecosistema |
| 14 | Cierre | Links, repos y próximos pasos |

## Demos en vivo

Guías paso a paso en [`demos/`](demos/):

- [`01-engram.md`](demos/01-engram.md) — Memoria persistente para agentes
- [`02-agentes-paralelos.md`](demos/02-agentes-paralelos.md) — Sub-agentes en paralelo
- [`03-skills.md`](demos/03-skills.md) — Contexto preciso bajo demanda
- [`04-sdd.md`](demos/04-sdd.md) — De idea a dashboard con SDD

## Navegación

| Acción | Teclas |
|--------|--------|
| Siguiente slide | `→`, `PageDown`, `Espacio` |
| Slide anterior | `←`, `PageUp` |
| Primer / último slide | `Home` / `End` |

También hay botones de anterior/siguiente y contador en la esquina inferior derecha, y una barra lateral con los módulos.

## Ejecutar localmente

No requiere instalación ni build. Cualquier servidor estático sirve:

```bash
git clone https://github.com/amalvarezme/IA-Agentes-Software.git
cd IA-Agentes-Software
python3 -m http.server 8000
```

Abre http://localhost:8000.

## Estructura

```
index.html            # Deck completo (todos los slides)
assets/css/styles.css # Estilos y tema visual LIA-UNAL
assets/js/app.js      # Navegación, teclado y contador
assets/images/        # Logo, diagramas y códigos QR
demos/                # Guías de demo en vivo
.github/workflows/    # Despliegue automático a GitHub Pages
```

## Despliegue

Cada push a `main` dispara el workflow [`pages.yml`](.github/workflows/pages.yml), que publica el sitio estático en GitHub Pages.
