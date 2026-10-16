# Blackjack Simulator

# 🃏 Blackjack

Juego de **Blackjack (21)** para el navegador: un jugador humano contra el ordenador (crupier). Proyecto full-stack con **Vue 3** en el frontend y **Node.js + Express** en el backend.

> 🚧 **Estado:** en desarrollo. Se construye paso a paso como proyecto de aprendizaje.

## ✨ Características

- Baraja de 52 cartas mezclada con el algoritmo Fisher-Yates.
- Reparto inicial de 2 cartas, con una del crupier boca abajo.
- Acciones del jugador: **pedir** carta o **plantarse**.
- El As vale 1 u 11 automáticamente según convenga.
- El crupier pide carta hasta alcanzar 17 o más.
- Resolución de victoria, derrota y empate.
- Lógica y estado de la partida en el servidor: la carta oculta del crupier nunca llega al navegador, así que no se puede hacer trampa desde las herramientas de desarrollo.

## 🧰 Tecnologías

| Capa | Tecnología |
|---|---|
| Frontend | Vue 3 (Composition API), Vite, JavaScript |
| Backend | Node.js, Express |
| Comunicación | API REST con JSON |

## 📁 Estructura

```
blackjack/
├── backend/
│   ├── server.js          # Servidor Express y rutas de la API
│   ├── pruebas/           # Scripts para probar la lógica
│   └── src/               # Carta, Baraja, Mano, Juego
└── frontend/
    └── src/
        ├── api/           # Llamadas al servidor
        ├── components/    # Componentes Vue
        └── App.vue
```

## 🚀 Instalación y uso

Requisitos: **Node.js 18 o superior**.

```bash
# 1. Clonar el repositorio
git clone https://github.com/TU_USUARIO/blackjack.git
cd blackjack

# 2. Backend (terminal 1)
cd backend
npm install
npm run dev

# 3. Frontend (terminal 2)
cd frontend
npm install
npm run dev
```

Abre `http://localhost:5173` en el navegador. El frontend redirige las peticiones `/api` al servidor en el puerto 3000 mediante el proxy de Vite.

## 🎮 Reglas implementadas

1. Jugador y crupier reciben 2 cartas.
2. Las cartas del 2 al 10 valen su número, J/Q/K valen 10 y el As vale 11 o 1.
3. El jugador pide o se planta. Si supera 21, pierde.
4. El crupier revela su carta y pide hasta llegar a 17 o más.
5. Gana quien más se acerque a 21 sin pasarse. Si hay igualdad, es empate.

## 🗺️ Hoja de ruta

- [ ] Clases `Carta` y `Baraja`
- [ ] Conexión Vue ↔ Express
- [ ] Clase `Mano` (lógica del As)
- [ ] Clase `Juego` (turnos y ganador)
- [ ] API: nueva partida, pedir, plantarse
- [ ] Interfaz con componentes Vue
- [ ] Estilos y animaciones
- [ ] Sistema de fichas y apuestas
- [ ] Doblar y dividir (split)

## 📄 Licencia

Distribuido bajo licencia MIT.
