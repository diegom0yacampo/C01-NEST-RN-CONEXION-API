# Ejercicio 05 · Mi primera conexión

## Cómo lo he montado

**Backend:**

cd backend
npm install
npm run start:dev

**Frontend**
cd frontend
npm install
npm start

## Qué he aprendido

- fetch() es lo que usa React Native para hacer una petición HTTP a un servidor, tal cual como haría el navegador.
- Hay que usara wait porque la respuesta no llega al momento, y sin await el código seguiría antes de tener el dato.
- .json() convierte la respuesta (que llega como texto) en un objeto de JS que ya puedo usar normal.
- Con setMensaje(...) guardo ese dato en el estado, y en cuanto lo hago, la pantalla se vuelve a pintar sola con el nuevo texto.

## Pregunta de comprensión

**¿Por qué el móvil necesita conocer la IP del equipo donde se ejecuta NestJS?**

Porque el móvil es un dispositivo distinto en la red, no es el mismo ordenador donde corre el backend. Si el móvil usara localhost, estaría intentando conectar consigo mismo, no con mi PC. Por eso necesita la IP real del ordenador en la red local para poder encontrarlo.

## Qué he modificado

De momento el ejercicio pedía solo que el botón conectara, cosa que ya hace.

## Resultado

Al pulsar "Conectar" me sale: **"Conexión establecida con NestJS 🎉"**, que es justo lo que devuelve el backend. O sea que backend y frontend están hablando de verdad entre ellos.

## Entrega

git add .
git commit -m "Ejercicio 05 - Mi primera conexion"
git push

