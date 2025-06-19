# Plan de Componentes, Rutas y APIs

Este documento resume la estructura inicial de la aplicación y las integraciones externas previstas.

## Componentes principales
- **AppLayout**: contenedor general con cabecera y navegación.
- **Feed**: muestra el flujo de publicaciones y looks recomendados.
- **Closet**: gestión del armario personal del usuario.
- **OutfitGenerator**: formulario para solicitar combinaciones a la IA.
- **Profile**: página de perfil de cada usuario.
- **LookCard**: tarjeta reutilizable para cada outfit o prenda.
- **Survey**: módulo para votaciones rápidas tipo "¿Cuál me pongo?".
- **ShoppingLink**: enlace de compra con imagen, precio y marca.

## Rutas de React
- `/` – `Feed`
- `/armario` – `Closet`
- `/crear-look` – `OutfitGenerator`
- `/perfil/:usuario` – `Profile`
- `/look/:id` – detalle de un look concreto

## Integración con APIs externas
1. **Catálogos de productos**: se consultarán mediante APIs REST de las marcas o mediante un feed de productos (CSV/JSON). Estas solicitudes se realizarán desde un backend que almacenará los resultados y filtrará por categoría o disponibilidad.
2. **Servicios de IA (ChatGPT/Jules.ai)**:
   - El front-end enviará las prendas seleccionadas y preferencias del usuario a un endpoint backend `/api/generate-look`.
   - El backend llamará a la IA con las imágenes, texto descriptivo o IDs de prendas para obtener la propuesta de outfit.
   - La respuesta incluirá combinaciones y enlaces sugeridos para que el front-end los muestre.
3. **Usuarios y autenticación**: se utilizará un servicio de autenticación (por ejemplo, Firebase Auth) para manejar inicios de sesión y perfiles.

Este plan sirve como punto de partida y podrá evolucionar a medida que se implementen nuevas funcionalidades.
