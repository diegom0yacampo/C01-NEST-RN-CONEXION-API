# Ejercicio 07 · Carga automática

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

- useEffect(() => { ... }, []) ejecuta lo que hay dentro **una vez**, justo cuando el componente aparece en pantalla, sin que el usuario tenga que hacer nada.
- El array vacío [] al final es importante: le dice a React que no repita ese efecto, que solo se ejecute la primera vez.

## Pregunta de comprensión

**¿Qué diferencia hay entre cargar los datos con un botón y cargarlos con useEffect?**

Con un botón, el dato solo llega si el usuario hace clic, no antes. Con useEffect y el array vacío, la carga pasa sola en cuanto se monta la pantalla, sin que nadie tenga que tocar nada. El botón sigue siendo útil para volver a pedir el dato más tarde, pero ya no hace falta para que aparezca la primera vez.

## Qué he modificado

Metido el useEffect para la carga automática y el estado cargando para el "Cargando…".

## Resultado

Al abrir la app, sale "Cargando…" un segundo y luego, sin tocar nada, pasa a 🟢 con el mensaje. El botón "Recargar" repite lo mismo si lo pulso.

## Entrega

git add .
git commit -m "Ejercicio 07 - Carga automatica"
git push
