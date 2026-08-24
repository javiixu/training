# Repo: dietas

## Objetivo

Generar **manualmente, cada semana**, dos archivos HTML distintos:

- Uno con la **dieta semanal** (comidas, macros, lista de la compra…)
- Otro con el **plan de ejercicio semanal** (sesiones, ejercicios, series/repes…)

Notas:

- El formato de estos HTML se irá refinando iterativamente; la prioridad ahora
  misma es tener el flujo de generación, no el diseño final.
- Al generar una nueva semana NO se sobreescriben las anteriores (histórico semanal).
- Skills del proyecto instaladas en `.opencode/skills/` (opencode las
  auto-carga; ver sección siguiente).

## Skills instaladas

En `.opencode/skills/` del proyecto (auto-cargadas por opencode):

### weekly-meal-planner

- Fuente: `github.com/marklavine-mlv/weekly-meal-planner` (MIT)
- Uso: plan semanal de comidas alrededor de la despensa habitual; plan editable
  de N días, lista de la compra agrupada por secciones, notas de preparación,
  recetas y estimación opcional de kcal/macros por plato.
- Flujo: lee (o pide) un `preferences.md` con hogar, reglas dietéticas, staples
  y objetivos de macros. Plantilla en `preferences.example.md` de la skill.

### coach-cards

- Fuente: `github.com/thomascaryzeng-maker/coach-cards` (MIT)
- Uso: plan de entrenamiento de fuerza personalizado a partir de una entrevista
  (objetivos, historial, lesiones, tiempo, material) y generación de una página
  HTML offline de un solo archivo (filtros, timer de descanso, log de pesos).
- Flujo: `interview -> profile.yaml -> plan.yaml -> build/coach.html`.
- Requisitos: Python 3.9+ con PyYAML (`pip install pyyaml` si falta).

### Nota sobre el objetivo HTML semanal

Estas skills son la base de generación, pero la salida final del repo es propia:
dos HTML semanales (dieta y ejercicio) cuyo formato se refinará aquí.
