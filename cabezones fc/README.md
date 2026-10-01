# Cabezones FC ULTRA — Render + Online

## Render
- Tipo: **Web Service**
- Runtime: **Node**
- Root Directory: `cabezones fc/` (si el repo tiene esa carpeta)
- Build Command: `npm install`
- Start Command: `npm start`

El servidor Express sirve el juego y el endpoint `/health`. El online usa PeerJS/WebRTC pasando por `/peerjs`; el host mantiene el estado del partido y sincroniza a los demás clientes.

## Cambios de esta versión
- Corregido el bug del jugador conectado que desaparecía: el host ahora marca cada slot como conectado en cuanto la conexión abre.
- Online 1v1 y 2v2 mantienen a todos los jugadores visibles y sincronizados.
- Tele-bola: **1 uso por cada gol de tu equipo**; se recarga al marcar.
- Salvación: te teletransporta a tu propio arco y crea una ventana corta para tapar el gol; **1 uso por cada gol de tu equipo**.
- Regate: recarga de **15 segundos**.
- Gol: se valida cuando el balón cruza **completamente** la línea de gol dentro del área de la portería.
- Añadidas comprobaciones de hitbox del marco/travesaño para rebotes fuera de la boca del arco.
- IA de MURO/RAYO mejorada: mejor predicción de trayectoria, posicionamiento, defensa de línea, salto e intención de remate según dificultad.
- La bola sigue teniendo recuperación automática cuando se queda atrapada en los pies.
