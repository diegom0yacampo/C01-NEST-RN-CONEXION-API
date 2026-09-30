# Ejercicio 09 · Busca superhéroe

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

- TextInput con value y onChangeText es un "campo controlado": cada letra que escribo actualiza el estado, y el campo siempre muestra lo que hay en ese estado, no al revés.
- Construyo la URL final concatenando: API_URL + /heroes/ + id. Si id vale 2, la petición real va a /heroes/2.
- keyboardType="numeric" hace que en el móvil salga el teclado numérico, aunque por dentro id siga siendo texto.
- Uso heroe && (...) para que la ficha solo se pinte si ya hay un héroe buscado. Mientras sea null, no se muestra nada.

## Pregunta de comprensión

**Sigue el valor id desde React Native hasta @Param('id'). ¿Por dónde pasa?**

Lo escribo en el TextInput, y onChangeText lo va guardando en el estado id. Al pulsar "Buscar", ese valor se pega dentro de la URL del fetch (por ejemplo /heroes/2). Esa petición llega al backend, @Get(':id') reconoce el 2 como la parte variable de la ruta, y @Param('id') lo coge y se lo pasa al método findOne, todavía como texto, antes de convertirlo a número con Number(id).

## Qué he modificado

Añadido el campo de ID, el botón "Buscar" y la ficha con nombre, poder y universo del héroe.

## Resultado

Escribo 2, le doy a Buscar, y me sale la ficha de Batman con su poder y universo.

## Entrega
git add .
git commit -m "Ejercicio 09 - Busca superheroe"
git push
