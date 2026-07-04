# Super Calculator

## Project overview
Calculadora Angular para fines educativos (ejercicios de estudiante). Los tres
ejercicios originales (toggle de signo, porcentaje, tema claro/oscuro) y las
pruebas unitarias pendientes ya fueron implementados en este fork.

## Tech stack
- Angular 19 (standalone components)
- TypeScript 5.7
- Karma + Jasmine para pruebas unitarias

## How to run
- Install: `npm install`
- Dev server: `npm start` → http://localhost:4200
- Tests: `npm test`

## Project structure
- `src/app/app.component.ts` — lógica del componente raíz (estado de la calculadora, handlers de botones)
- `src/app/app.component.html` — template
- `src/app/app.component.css` — estilos, incluye reglas de modo claro/oscuro
- `src/app/app.component.spec.ts` — suite de pruebas (Karma + Jasmine)
- `karma.conf.js` — configuración del test runner
- `requirements.md` — enunciado original de los ejercicios de estudiante

## Exercises
Ejercicios originales, ya resueltos:
- `pressToggleSign()` — invierte el signo del número mostrado
- `pressPercent()` — divide el número mostrado entre 100
- `toggleTheme()` — alterna modo oscuro/claro (incluye `host: { '[class.light]': 'isLightMode' }` en el componente para que `:host.light` aplique)

## Coding conventions
- Comentarios explicativos orientados a enseñanza (el código está pensado para que un estudiante lo lea)
- Los tests siguen el patrón: llamar métodos del componente → `fixture.detectChanges()` → leer `.display__value` o propiedades del componente
- Cada parte del ejercicio vive en su propia branch (`exercise-1-part-1`, `exercise-2-part-2`, `exercise-3-part-3`, ...), pensada para un PR independiente; `main` se mantiene igual al repo original
