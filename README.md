# Conversa — subtítulos en vivo para la abuela

Webapp que transcribe conversaciones en tiempo real en español (castellano),
**distinguiendo quién habla** (cada persona con su color y su nombre), pensada
para personas sordas. No guarda nada: al cerrar la app la conversación se borra.

Usa la API de streaming de Deepgram (modelo Nova-3, `language=es`, `diarize=true`).

## Puesta en marcha (una sola vez)

1. **Clave de Deepgram**: crea una cuenta en https://console.deepgram.com
   (regalan 200 $ de saldo; a ~0,41 $/hora dan para más de 480 horas de uso).
   En *API Keys* → *Create a New API Key*, copia la clave.
2. **Publicar la webapp** (necesita HTTPS para que Chrome permita el micrófono).
   Opciones gratuitas:
   - **GitHub Pages**: sube esta carpeta a un repositorio y activa Pages.
   - **Netlify Drop** (https://app.netlify.com/drop): arrastra la carpeta y listo.
3. **En la tablet**: abre la URL en Chrome → menú ⋮ → **"Añadir a pantalla de
   inicio"**. Queda instalada como una app a pantalla completa.
4. Abre la app → ⚙️ Ajustes → pega la clave → Guardar.

## Uso

- Botón verde **🎤 Empezar**: empieza a subtitular. Cada persona sale en una
  burbuja de un color («Persona 1», «Persona 2»…).
- Tocar el nombre de una burbuja permite ponerle el nombre real («Marta»,
  «Abuela»…). Los nombres solo duran esa sesión.
- **A− / A+**: tamaño de letra. **🌙/☀️**: tema oscuro o claro.
- **🗑️**: borra la conversación (pide confirmación con un segundo toque).
- La pantalla se mantiene encendida mientras escucha, y si se corta el wifi
  reconecta sola.

## Modo demostración

Para probar la interfaz sin clave ni micrófono: ⚙️ Ajustes → **Ver
demostración**, o abre la URL con `?demo=1`.

## Privacidad

- El audio se envía en streaming a Deepgram solo para transcribirlo; con la
  configuración por defecto del proyecto no se almacena el audio de forma
  permanente (opción `mip_opt_out` disponible en la cuenta para desactivar
  también el programa de mejora de modelos).
- La transcripción vive solo en la memoria de la pestaña: cerrar = borrar.
- En la tablet solo se guardan la clave de API y las preferencias (letra, tema).

## Coste

Deepgram Nova-3 en español con diarización: ~0,41 $/hora (tarifa promocional
verificada en agosto de 2026). Uso típico de 30–60 h/mes ≈ 12–25 $/mes, pero los
200 $ de crédito inicial cubren aproximadamente el primer año.
