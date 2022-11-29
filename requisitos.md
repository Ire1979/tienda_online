# Recuperar todo los productos

- URL:  GET /api/products
    - Responder con status 200
    - Respuesta debe tener formato JSON
    - Respuesta debe ser un array de productos


# Crear un producto

- URL: POST /api/products
    - Responder con status 200
    - Respuesta debe tener formato JSON
    - Comprobar si tiene _id
    - Comprobar si el producto en la BD tiene el mismo nombre con el que lo hemos insertado


# Actualizar un producto

- OBJETICO: Lanzar una petición pasándole el ID del producto a editar y los datos que quiero editar
- PREVIO: Necesito crear un objeto para poder editarlo a posteriori
- FINAL: Borraremos ese objeto

- URL: /api/products/:productId
    - Status 200 y Content-Type application/json
    - Comprobar quee los campos que modificamos, realmente se modifican en la BD

- Crear la URL
- Método findByIdAndUpdate
    - De dónde saco el ID?
    - De dónde saco el obajeto para editar?
- Responder con un JSON con lo que devuelva el método anterior
- ¡¡¡¡¡ La última prueba FALLA !!!!!


# Borrar un producto

- Una URL que me permita borrar un producto
- URL : /api/products/:productId
    - PREVIO: Creamos un producto en la BD
    - FINAL: Borramos el producto creado por si no funciona la prueba
- Comprobamos si la URL existe
- Comprobamos si el producto sigue en la BD


# CLIENTES

1. Creación del modelo de client (client.model.js)
- name, email, address, age(NUMBER), active (BOOLEAN)

2. Rutas para el manejo de los clientes
- GET /api/clients - find
- POST /api/clients - create
- PUT /api/clients/:clientId - findByIdAndUpdate
- DELETE /api/clients/:clientId - findByIdAndDelete

## NO OLVIDAR

- Hay que conectar api.js con el nuevo fichero clients.js
- Las pruebas las hacemos arrancando el proyecto y a través de peticione.rest