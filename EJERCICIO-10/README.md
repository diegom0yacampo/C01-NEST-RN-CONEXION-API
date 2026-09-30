# Ejercicio 10 · Likes

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

- fetch por defecto siempre hace GET. Para hacer otro tipo de petición (en este caso PATCH) hay que indicarlo a mano con un segundo parámetro: { method: 'PATCH' }.
- Aprendí también que un @Patch(':id/like') no se puede probar poniendo la URL en el navegador, porque eso siempre hace GET. Hay que probarlo desde la propia app.

## Pregunta de comprensión

**¿Por qué se usa PATCH y no GET para dar like?**

Porque GET está pensado solo para leer datos, no para cambiarlos. PATCH indica que la petición va a modificar algo que ya existe en el servidor. Si dar like fuera un GET, cualquier cosa que recargue esa URL sin querer (el navegador, una caché) podría sumar likes solo, sin que el usuario lo haya pedido de verdad.

## Qué he modificado

Añadido el corazón con el contador de likes y el botón "Me gusta" que hace la petición PATCH.

## Resultado

Al abrir la app sale Rocky con 0. Cada vez que le doy a "Me gusta" el número sube: 1, 2, 3... y se mantiene mientras el backend siga encendido.

## Entrega
git add .
git commit -m "Ejercicio 10 - Likes"
git push