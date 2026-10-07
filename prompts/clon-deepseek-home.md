# Prompt: clon de frontend y UX/UI de la página de inicio de DeepSeek

## Objetivo

Reproducir visualmente la página de inicio de https://www.deepseek.com/en/ con el mismo stack tecnológico que usa el sitio original. El alcance es solo presentación: estructura HTML, estilos, animaciones, interacciones de UI y diseño responsive.

"100% igual, pixel perfect" se traduce en un criterio medible: la diferencia visual contra las capturas de referencia debe quedar por debajo del umbral definido en la sección de criterios de aceptación. Un clon idéntico al píxel en todos los navegadores y anchos no es realista, y el umbral deja claro qué se considera aceptable.

## Alcance

**Incluye**
- Cabecera y navegación (incluidos menús desplegables y menú móvil).
- Hero y todas las secciones de la home, en el orden original.
- Pie de página.
- Estados `hover`, `focus` y `active`, y las animaciones visibles en la página.
- Comportamiento responsive en los breakpoints de referencia.

**Excluye**
- Backend, autenticación, chat, API, formularios reales y analítica.
- Cualquier llamada a servicios de DeepSeek. Usar datos estáticos o mocks.
- Otras páginas del sitio, salvo que se pidan explícitamente.

## Restricciones legales y de marca

- No copiar logotipos, marcas ni imágenes con copyright. Usar placeholders o SVG genéricos.
- No publicar el resultado como sitio oficial ni sugerir afiliación con DeepSeek. Si se publica, cambiar nombre, textos y marca.
- Respetar los términos de uso del sitio y su `robots.txt`. No hacer scraping masivo: capturar solo las páginas necesarias para la referencia.
- Si el proyecto es personal o de estudio, el texto original puede reutilizarse. Si se publica, reemplazarlo.

## Stack tecnológico

1. **Antes de elegir tecnologías, inspeccionar el sitio original.** Identificar framework (React, Next.js, Vue, Nuxt, etc.), bundler, sistema de CSS (Tailwind, CSS Modules, styled-components, CSS puro), fuentes y librerías de animación. Revisar el HTML renderizado, los recursos cargados en la pestaña Network y los estilos computados.
2. **Documentar los hallazgos** en `docs/analysis.md`, indicando qué se confirmó y qué se infirió.
3. **Usar el stack identificado.** Si no se puede determinar con certeza algún elemento, decirlo explícitamente, proponer la alternativa más cercana y justificarla.

## Proceso

### Fase 1: referencia
- Capturar la página completa en anchos de **1440, 1024, 768 y 390 px**. Guardar en `reference/`.
- Si la página tiene modo claro y oscuro, capturar ambos.

### Fase 2: extracción de tokens
Medir y registrar en `docs/tokens.md`:
- Tipografía: familias, tamaños, pesos, interlineado y tracking.
- Paleta: valores hex o rgb exactos.
- Espaciados, radios, sombras, anchos máximos, breakpoints y `z-index`.

### Fase 3: construcción
- Construir de arriba hacia abajo: cabecera, hero, secciones, pie.
- Crear variables CSS o tokens del framework con los valores de la fase 2. No usar valores "a ojo".
- Responsive desde el inicio, no como parche al final.

### Fase 4: comparación
- Comparar cada breakpoint con su captura de referencia, por sección y por página completa.
- Generar capturas comparativas y mapas de diferencias. Guardarlos en `reports/`.
- Corregir las diferencias por encima del umbral y repetir la comparación.

## Criterios de aceptación

- **Diferencia visual:** menos de **1 %** de píxeles distintos por breakpoint (por ejemplo, con `pixelmatch` u otra herramienta equivalente, con el umbral documentado en el reporte).
- **Responsive:** sin scroll horizontal en 390 px. Ningún elemento se corta ni se superpone.
- **Interacción:** estados `hover`, `focus` y `active` equivalentes a los del original. El menú móvil abre y cierra correctamente.
- **Accesibilidad:** contraste WCAG AA, navegación completa por teclado, `alt` en imágenes, etiquetas en botones de icono y semántica correcta (`header`, `nav`, `main`, `footer`).
- **Rendimiento:** Lighthouse de rendimiento y accesibilidad de **90 o más** en escritorio.
- **Calidad:** `npm run build` (o el comando del stack) sin errores ni advertencias, y sin errores en la consola del navegador.

## Entregables

1. Código del clon dentro del repositorio, en una carpeta propia (por ejemplo, `clones/deepseek-home/`).
2. `docs/analysis.md` y `docs/tokens.md`.
3. Capturas de referencia y reportes de comparación en `reference/` y `reports/`.
4. `README.md` con: stack usado, cómo instalar y ejecutar, cómo repetir la comparación visual y decisiones tomadas.
5. Lista breve de diferencias conocidas que no se pudieron eliminar, con su causa.

## Formato de trabajo esperado

1. Plan breve con las fases y los riesgos principales (por ejemplo, fuentes propietarias o contenido generado por JavaScript).
2. Implementación por fases, con verificación visual al final de cada una.
3. Resumen final con: qué se logró, qué umbrales se cumplen, qué diferencias quedan y por qué.
