# Ejercicio 11 · Mini tienda

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

- @Post() sin nada dentro sigue apuntando a la misma ruta que el @Get() (/productos). Lo que cambia entre uno y otro no es la URL, es el verbo HTTP.
- @Body() coge el cuerpo de la petición (el JSON que mando desde el móvil) y me lo da ya convertido en objeto, sin que tenga que parsear nada a mano.
- Para mandar el cuerpo tengo que poner el header 'Content-Type': application/json', para que el backend sepa que lo que le llega es JSON.
- fetch siempre manda el body como texto, así que hay que usar JSON.stringify({...}) antes de mandarlo. En el backend, Nest lo vuelve a convertir en objeto automáticamente gracias al @Body().

## Pregunta de comprensión

**¿Qué recorrido realiza el objeto hasta llegar a @Body()?**

El objeto nace como dos estados sueltos en el móvil (nombre y precio). Al pulsar "Añadir" los junto en un objeto y JSON.stringify lo convierte en texto para que pueda viajar dentro del body del fetch. Esa petición POST llega al backend, y @Body() recoge ese texto, lo vuelve a convertir en objeto de JS, y se lo pasa al método crear para que lo procese y lo añada al array.

## Qué he modificado

Añadidos los campos de nombre y precio, el botón "Añadir" y la actualización automática de la lista después de crear el producto.

## Resultado

Escribo un nombre y un precio, le doy a Añadir, y el producto nuevo sale al momento en la lista de arriba.

## Entrega
git add .
git commit -m "Ejercicio 11 - Mini tienda"
git push