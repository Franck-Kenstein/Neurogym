# NeuroGym – Entrenamiento cerebral

App web (PWA) con 370 juegos y 5 niveles de dificultad (1350 ejercicios) para entrenar memoria, velocidad, atención, lenguaje, lógica, flexibilidad mental, cálculo, visoespacial y multitarea y auditiva. Funciona sin internet y guarda tu progreso en el navegador con perfiles de usuario, récords, logros y ranking local (puntajes, racha, historial por juego).

**Creada y diseñada por Francisco Javier Torres Vélez.** © 2026. Todos los derechos reservados (ver `LICENSE`).

## Archivos
- `index.html`: la app completa (HTML, CSS y JavaScript en un solo archivo)
- `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`: instalación como app y modo sin conexión
- `LICENSE`, `.nojekyll`, `.gitignore`

## Usarla en local
Abre `index.html` en el navegador. Para probar la instalación como app, sírvela con un servidor local (por ejemplo `python3 -m http.server`) y abre `http://localhost:8000`.

## Publicar en GitHub Pages
1. Crea un repositorio nuevo en GitHub y sube todos estos archivos a la rama `main`.
2. En el repositorio: Settings → Pages → Build and deployment → Source: *Deploy from a branch* → Branch: `main` / `(root)` → Save.
3. En uno o dos minutos tendrás la dirección `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

## Publicar en Netlify
Arrastra esta carpeta completa a https://app.netlify.com/drop (mejor con cuenta gratuita para que el sitio no caduque).

## Instalar en Android
- Abre la dirección publicada en Chrome → menú → *Instalar app* / *Añadir a pantalla de inicio*.
- APK: entra a https://www.pwabuilder.com, pega la dirección publicada y sigue *Package for stores → Android*.
- Alternativa: Android Studio con un `WebView` que cargue `file:///android_asset/index.html` (activa `javaScriptEnabled` y `domStorageEnabled`).

## Notas
- Perfiles, récords y logros se guardan en el navegador del dispositivo (sin servidor). Usa «Respaldo» en Mi perfil para llevarlos a otro dispositivo.
- Los juegos de fluidez verbal cuentan las palabras que escribes; solo validan terminaciones o letra inicial, no hay diccionario completo.
- *Adivina la palabra* acepta únicamente las palabras de su lista interna.
- Esta app es de entrenamiento y entretenimiento; no es una herramienta médica.
- Sincronización entre dispositivos (opcional): en Mi perfil → Sincronizar, con un proyecto gratuito de Firebase (plan Spark, sin tarjeta): Authentication por correo + Firestore con reglas por usuario. Para no escribir apiKey y projectId en cada dispositivo, ponlos en la constante `FBC` al inicio del bloque de sincronización de `index.html`. No funciona dentro de claude.ai.
- Dificultad adaptativa (botón en la pantalla de inicio): ajusta el nivel de cada juego según tus resultados. Se puede saltar cualquier juego y elegir categorías o juegos concretos, en orden o al azar.

~~~~~~
