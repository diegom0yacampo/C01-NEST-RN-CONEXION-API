# Ejercicio 06 · Estado de conexión

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

- Se pueden tener varios useState a la vez en el mismo componente, cada uno guardando una cosa distinta. Aquí tengo uno para el mensaje y otro para saber si estoy conectado (`true/false).
- La gracia de useState frente a una variable normal es que React se entera cuando cambia. Si hiciera let conectado = false y luego conectado = true, la pantalla no se enteraría de nada. Con setConectado(true) sí, porque eso avisa a React de que tiene que repintar.
- Con un simple operador ternario (conectado ? '🟢' : '🔴') puedo mostrar una cosa u otra según el estado, sin tener que hacer un if gigante.

## Pregunta de comprensión

**¿Qué aporta UseState frente a una variable normal?**

Que React se entera cuando cambia el valor. Una variable normal puede cambiar por dentro pero la pantalla no se actualiza sola; con useState, en cuanto llamo a la función set..., React vuelve a ejecutar el componente y pinta la pantalla con el valor nuevo, sin que yo tenga que hacer nada más.

## Qué he modificado

Añadido el segundo estado conectado y el texto que cambia entre 🔴 y 🟢 según si ya se ha hecho la petición o no.

## Resultado

Al abrir la app sale 🔴 y "Sin conectar". Al pulsar el botón, pasa a 🟢 y el mensaje del backend. Tal cual tenía que ser.

## Entrega

git add .
git commit -m "Ejercicio 06 - Estado de conexion"
git push
