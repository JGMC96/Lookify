# Lookify – Tu estilista social con IA

Lookify es una aplicación web que combina inteligencia artificial, moda real y el poder de la comunidad para ayudarte a decidir qué ponerte y descubrir nuevas prendas.

## Características principales
- **Mi Armario digital**: organiza tus prendas por categorías y genera looks solo con lo que ya tienes.
- **Sugerencias automáticas de outfits**: la IA mezcla tus prendas con recomendaciones de tiendas online y proporciona enlaces directos de compra.
- **Funciones sociales**: comparte tus looks, recibe opiniones con encuestas y participa en desafíos semanales de estilo.
- **Filtros inteligentes**: personaliza los resultados por estilo, clima, ocasión o colores favoritos.
- **Modelo de monetización**: enlaces afiliados, publicidad integrada y plan premium con extras exclusivos.

## Plan de componentes y rutas
- `/` – feed principal con los looks recomendados y publicaciones de la comunidad.
- `/armario` – componente **Closet** para gestionar las prendas guardadas y subir nuevas fotos.
- `/crear-look` – componente **OutfitGenerator** para solicitar sugerencias de la IA.
- `/perfil/:usuario` – componente **Profile** con publicaciones, seguidores y armario público.
- Otros componentes: **LookCard**, **Survey**, **ShoppingLink**, entre otros.

## Integración con APIs y servicios de IA
- Conexión a catálogos de marcas mediante APIs REST o feeds de productos para obtener imágenes, nombres y precios.
- Comunicación con servicios de IA (ChatGPT o Jules.ai) a través de un backend que reciba las prendas del usuario y devuelva las combinaciones sugeridas.
- El front-end consume estas sugerencias desde endpoints propios (`/api/outfits`, `/api/items`) y muestra las prendas con enlaces directos de compra.

## Desarrollo
Este proyecto usa [Vite](https://vitejs.dev/) y [React](https://react.dev). Para ejecutar el entorno de desarrollo:

```bash
npm install
npm run dev
```

Para ejecutar los tests unitarios:

```bash
npm test
```

Para ejecutar el linter:

```bash
npm run lint
```

Esto ejecuta ESLint utilizando la configuración del proyecto.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
