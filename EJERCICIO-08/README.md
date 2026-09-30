# Ejercicio 08 · Menú del restaurante

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

- FlatList recorre un array entero y pinta un elemento por cada objeto, sin que yo tenga que escribir un <Text> a mano por cada producto.
- data={productos} es el array que le paso, keyExtractor le dice cómo identificar cada elemento (para que React sepa cuál es cuál), y renderItem es la función que decide cómo se ve cada fila.

## Pregunta de comprensión

**¿Qué relación existe entre el array del Service y data={productos}?**

El array del Service es la fuente original de los datos en el backend. Cuando el móvil hace el fetch, recibe ese mismo array convertido en JSON y lo guarda en su propio estado (que también llamo productos). El data={productos} le dice a FlatList que use justo esos datos para generar la lista, uno por uno.

## Qué he modificado

Convertido cada producto en tarjeta (emoji + nombre + precio con estilo) y añadida una cuarta comida (Ensalada) en el array del Service.

## Resultado

Salen las 4 tarjetas del menú, cada una con su emoji, nombre y precio.

## Entrega

git add .
git commit -m "Ejercicio 08 - Menu del restaurante"
git push