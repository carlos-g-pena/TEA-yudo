<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://ai.google.dev/static/site-assets/images/share-ais-513315318.png" />
</div>

# Run and deploy your AI Studio app

This contains everything you need to run your app locally.

View your app in AI Studio: https://ai.studio/apps/b7d88625-a17a-4b8f-8d70-7ff4903ac001

## Run Locally

**Prerequisites:**  Node.js


1. Install dependencies:
   `npm install`
2. Set the `GEMINI_API_KEY` in [.env.local](.env.local) to your Gemini API key
3. Run the app:
   `npm run dev`

## Cuentas profesionales y estudiantes (modo local)

- **Profesional**: crea su cuenta con correo, contraseña y un PIN de 4 dígitos. La contraseña y el PIN se guardan con hash PBKDF2-SHA256 (Web Crypto), por lo que la app debe abrirse por HTTPS o `localhost` (AI Studio ya usa HTTPS).
- **Estudiantes**: no tienen cuenta. Cada profesional crea y gestiona a sus estudiantes desde la pestaña **Estudiantes**. Comunicador, agenda, fotos personalizadas y bitácora se guardan por separado para cada estudiante.
- **Accesos**: al pulsar **Iniciar sesión** en un estudiante se registra un acceso (inicio, término, duración y frases/emociones/rutinas realizadas) y el área profesional queda bloqueada con el PIN. El historial se puede exportar a CSV.
- **Limitación**: todo vive en el `localStorage` del navegador. Las cuentas y los datos solo existen en ese dispositivo, no se sincronizan y no hay recuperación de contraseña. Borrar los datos del navegador borra las cuentas.
