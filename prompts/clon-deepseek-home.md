# Prompt: página de inicio original inspirada en el análisis de la home de DeepSeek (tarea universitaria)

## Objetivo

Construir una página de inicio **original** con el mismo stack tecnológico que usa la home de https://www.deepseek.com/en/, aplicando el análisis de su estructura, su jerarquía visual y su comportamiento responsive. El resultado debe ser una réplica de **técnica y de estructura de layout**, no una copia de sus recursos. Para la entrega académica, el criterio de éxito es la fidelidad de la estructura medida con datos, no la igualdad píxel a píxel con el sitio original.

## Por qué no se copia el sitio original

Una copia al 100 % de la página de DeepSeek incluye su código fuente, logotipos, imágenes, tipografías licenciadas y textos protegidos por derechos de autor. Eso no es un ejercicio de análisis y no debe producirse ni entregarse. Este prompt está pensado para que el alumno demuestre que entiende el stack, el sistema de diseño y el responsive, y que puede reproducir esas decisiones con contenido propio.

Si la cátedra exige fidelidad visual alta, hay alternativas válidas:
- Usar un mockup o diseño que la cátedra entregue por escrito.
- Clonar un sitio con licencia abierta (por ejemplo, un template MIT o Creative Commons) y documentar la licencia.
- Pedir confirmación a la cátedra antes de empezar.

## Alcance

**Incluye**
- Cabecera con navegación, menú desplegable y menú móvil.
- Hero y las secciones de la home, en el mismo orden y con la misma jerarquía de contenido.
- Pie de página.
- Estados `hover`, `focus` y `active`, y animaciones de entrada sencillas.
- Diseño responsive en los breakpoints de referencia.

**Excluye**
- Backend, autenticación, chat, API, formularios reales y analítica.
- Llamadas a servicios de DeepSeek. Usar datos estáticos.
- Otras páginas del sitio.

## Reglas de contenido y marca

- **Logotipo, nombre y marca:** usar un nombre ficticio y un logotipo propio o un placeholder genérico.
- **Imágenes e iconos:** crearlos propios o usar una librería con licencia abierta (por ejemplo, Lucide o Heroicons, MIT). No descargar imágenes del sitio original.
- **Textos:** redactar contenido original para cada sección. Mantener la longitud y la jerarquía aproximadas, no las frases.
- **Tipografía:** usar fuentes con licencia abierta (por ejemplo, Google Fonts) y declarar cuál.
- **No sugerir afiliación** con DeepSeek ni usar su nombre de forma que induzca a error. La página debe llevar un aviso de que es un trabajo académico sin relación con la empresa.

## Stack tecnológico

1. **Identificar el stack del sitio original** antes de elegir herramientas: framework, bundler, sistema de CSS y librerías de animación. Revisar el HTML renderizado y la pestaña Network. Documentar en `docs/analysis.md` qué se confirmó y qué se infirió.
2. **Usar ese mismo stack** para el proyecto. Si algún elemento no se puede determinar con certeza, decirlo y justificar la alternativa.
3. El análisis técnico (estructura, responsive, tokens) puede describirse con detalle. El código y los recursos deben ser propios.

## Proceso

### Fase 1: análisis de estructura
- Capturar la página original en **1440, 1024, 768 y 390 px** solo como referencia para la cátedra. No se incluye en el repositorio.
- Describir por escrito cada sección: posición, jerarquía, número de columnas, alturas aproximadas y comportamiento al cambiar de ancho.

### Fase 2: tokens propios
Definir en `docs/tokens.md` una paleta, una escala tipográfica, espaciados, radios y breakpoints **propios**, inspirados en las proporciones medidas en la fase 1. No copiar los valores exactos de colores ni de fuentes si tienen marca registrada.

### Fase 3: construcción
- Construir de arriba hacia abajo: cabecera, hero, secciones, pie.
- Usar variables CSS o tokens del framework.
- Responsive desde el inicio.

### Fase 4: verificación de estructura
- Medir en el proyecto propio la posición y el tamaño de los bloques principales (cabecera, hero, columnas, pie) en cada breakpoint.
- Comparar esas medidas con las de la fase 1 y registrar las diferencias en `reports/`. El objetivo es que la estructura se parezca, no que los píxeles coincidan.

## Criterios de aceptación

- **Estructura:** las secciones aparecen en el mismo orden y con la misma jerarquía. Las posiciones de los bloques principales difieren menos de **±8 px** en cada breakpoint (medido en `reports/`).
- **Responsive:** sin scroll horizontal en 390 px. Ningún elemento se corta ni se superpone.
- **Interacción:** `hover`, `focus` y `active` presentes en todos los elementos interactivos. El menú móvil abre y cierra con teclado y con ratón.
- **Accesibilidad:** contraste WCAG AA, navegación completa por teclado, `alt` en imágenes, etiquetas en botones de icono y semántica (`header`, `nav`, `main`, `footer`).
- **Rendimiento:** Lighthouse de rendimiento y accesibilidad de **90 o más** en escritorio.
- **Calidad:** el comando de build del stack termina sin errores ni advertencias, y la consola del navegador no muestra errores.
- **Originalidad:** ningún logotipo, imagen, icono ni texto del sitio original aparece en el repositorio. Se verifica con una búsqueda en el código y en los recursos.

## Entregables

1. Código del proyecto en una carpeta propia (por ejemplo, `proyectos/home-universidad/`).
2. `docs/analysis.md` (estructura y stack) y `docs/tokens.md` (tokens propios).
3. `reports/` con la comparación de estructura por breakpoint.
4. `README.md` con: stack, instrucciones para instalar y ejecutar, licencias de fuentes e iconos, aviso de trabajo académico y decisiones tomadas.
5. Lista de diferencias respecto al original y su motivo.

## Formato de trabajo esperado

1. Plan breve con las fases y los riesgos principales.
2. Implementación por fases, con verificación al final de cada una.
3. Resumen final con: qué se logró, qué criterios se cumplen y qué diferencias quedan.
