# NeuroGym v9 (2.ª entrega)

## Subir
`index.html` + `sw.js` (caché `neurogym-v12`) a GitHub. Abre la app dos veces.

## OBLIGATORIO: reglas nuevas
Firebase → Firestore → Reglas → pega `REGLAS_FIRESTORE_v9.txt` → Publicar.
Sin esto el torneo y los duelos darán error 403.

## Anti-trampa (torneo y duelos)
- Al pulsar «Empezar» la app crea un documento de inicio con la hora del SERVIDOR (`tstart` / `dstart`), de un solo uso: no se puede reintentar ni ver las preguntas y volver a empezar.
- El resultado solo se acepta si: puntos entero 0–100, tiempo 3 s–15 min, y el tiempo reportado coincide con el tiempo real transcurrido en el servidor (tolerancia 20 s). Un tiempo inventado o un resultado sin inicio es rechazado por las reglas.
- Límite honesto: sin servidor propio (Cloud Functions requiere plan de pago) NO se puede comprobar que los puntos vengan de respuestas reales. Un tramposo técnico que automatice respuestas correctas a velocidad humana aún podría pasar. El ranking global (`pts`) tampoco está blindado.
- No probado contra Firebase real (solo servidor simulado): si el torneo da error tras publicar las reglas, avísame con el mensaje exacto.

## Retos (Inicio → 🎯) — actualizado
- 4 retos por día, de 4 tipos distintos (partidas, puntaje, juego concreto, récords/monedas), iguales para todos los jugadores ese día. Premios: monedas + XP de mascota; bonus +100 🪙 y posible objeto gratis al reclamar los 4.
- Sin fecha final y sin repetirse: verificado 1500 días seguidos con 0 repeticiones. Cuando se agota un carril (180, 850, 810 y 74 días) los retos suben de meta o de nivel mínimo en vez de repetirse.
- Con el paso de los meses algunas metas se vuelven más exigentes; puedes dejar un reto sin cumplir.

## Sin ventajas en el ranking mundial
- Mascotas, habilidades, escudo, retos y objetos solo afectan monedas, XP y cosméticos.
- El escudo ya NO cambia el puntaje: el error cuenta igual para tu récord y el ranking; solo protege las monedas de esa partida.
- Torneo y duelos: sin escudo ni ventajas.

## Aro del avatar (menú principal), 2 cambios a la vez
- Aro de color/grosor/velocidad según el nivel de la mascota (Nv 1, 10, 25, 50, 75, 100).
- Estrellas orbitando según retos cumplidos (3, 10, 25, 60, 120, 250).

## Juegos: 240 → 270 (27 por categoría, +3 cada una)
Memoria: m9Max, m9Emo, m9Pal · Velocidad: v9Sum, v9May, v9Cer · Atención: a9Imp, a9Con, a9May · Lenguaje: f9Fin, f9Cor, f9Rep · Lógica: l9Fib, l9Cua, l9Ari · Flexibilidad: c9Tri, c9Mas, c9Dif · Cálculo: n9Su3, n9Pot, n9Cub · Visoespacial: e9Are, e9Lad, e9Hue · Multitarea: mtMesPar, mtTrAn, mtCuVo · Auditiva: a9Triple, a9Dif, a9Baja.

## No verificado
Android real, Firebase real, sonido en el teléfono.
