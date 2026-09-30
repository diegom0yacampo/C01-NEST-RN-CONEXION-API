# Ejercicio 12 · Creature Lab (el final)

## Cómo lo he montado

**Backend:**
cd backend
npm install
npm run start:dev

**Frontend:**
cd frontend
npm install
npm start

## Qué he aprendido

Más que aprender algo nuevo, aquí lo que hice fue ver cómo encajan todas las piezas de golpe:

- La FlatList de arriba pinta el listado completo de criaturas, igual que hacía con las pizzas o el menú.
- El campo de texto + botón "Buscar" hace lo mismo que en el ejercicio del superhéroe, solo que ahora guardo el resultado en seleccionada en vez de heroe.
- El botón "Me gusta" de la ficha hace el PATCH, igual que con las mascotas, pero aquí además de actualizar la ficha también vuelvo a llamar a cargarCriaturas(), para que el número de likes se actualice también en la lista de arriba, no solo en la ficha.

## Pregunta de comprensión

**¿Podrías explicar el viaje completo de un dato sin mirar el código?**

Vale, esta es la del resumen de todo el cuaderno. Los datos nacen como un array temporal dentro del Service. El Controller expone ese array (o partes de él) a través de rutas HTTP: GET para leer, PATCH para modificar. Desde React Native, hago un fetch() a esa ruta, la respuesta me llega como texto y la convierto en objeto con .json(). Ese objeto lo guardo en un useState, y React usa ese estado para pintar la pantalla. Cada vez que interactúo con la app (busco algo, doy like), se repite el mismo ciclo: petición nueva, respuesta nueva, estado nuevo, pantalla nueva.

## Qué he modificado

Junté el listado, la búsqueda y el sistema de likes en una sola pantalla, con una interfaz sencilla: título arriba, lista de criaturas, buscador por id, y ficha con botón de like debajo.

## Resultado

Salen las 3 criaturas con 0 likes cada una. Busco por id, me sale la ficha, le doy a "Me gusta" varias veces y el contador sube tanto en la ficha como en la lista de arriba.

## Entrega
git add .
git commit -m "Ejercicio 12 - Creature Lab"
git push