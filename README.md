# Team Builder

## Problema

En los grupos de basket, cuando el partido está muy decantado para un equipo, se vuelve poco disfrutable para los jugadores. Generalmente esta responsabilidad queda sujeta a la subjetividad de una persona en particular y puede ser cuestionable.

## Solución

La idea de este proyecto es proporcionar una UI para la creación de equipos de basket balanceados, considerando:

- Niveles de juego
- Características de jugadores
- Preferencias personales en cuanto a compañeros
- Una lista de jugadores fijos con un rating dinámico
- Actualizaciones pos-partido
- Posibilidad de agregar jugadores no regulares

La aplicación esta pensada para ser operada por el administrador del grupo, si bien esta pensada para equipos de basket, a futuro podría contemplar otros deportes en grupo como futbol 5/7 también.

## Stack

- _Frontend_: React + TypeScript + Tailwind.
- _Estado_: Zustand.
- _Enrutamiento_: Voy a probar Tanstack Router, usualmente uso react-router.
- _Backend_: Eventualmente Firestore o MongoDB, a definir.

## Roadmap

### Fase 1: Core Funcional

- [ ] _MVP con localStorage_  
       Crear/editar jugadores y asignarlos manualmente a equipos.
- [ ] _Algoritmo de rating básico_  
       Calcular puntos por victoria/MVP y actualizar perfiles.
- [ ] _Generación automática de equipos (versión simple)_  
       Balanceo por rating sin restricciones/preferencias.

### Fase 2: Experiencia de Admin

- [ ] _Ajustes manuales post-generación_  
       Intercambiar jugadores entre equipos.
- [ ] _Template para WhatsApp_  
       Botón que copie equipos en formato texto.
- [ ] _Jugadores no regulares_  
       Agregar "invitados" sin afectar el balanceo.

### Fase 3: Escalabilidad

- [ ] _Auth + DB (Firestore/MongoDB)_  
       Login y aislamiento de datos por usuario.
- [ ] _Algoritmo avanzado_  
       Balanceo con restricciones + preferencias.
      Restricciones: Jugador A no puede jugar con Jugador B.
      Preferencias: De ser posible, Jugador A quiere jugar con Jugador C.
- [ ] _Historial de partidos_  
       Equipo ganador y mvps por equipo.
