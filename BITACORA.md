##p0 
El navegador web (o herramientas como Thunder Client / Postman).
Nuestra aplicación de Node.js corriendo en la computadora.
Un Request (petición) con el método HTTP (GET/POST), la URL y los encabezados.
Un Response (respuesta) con un código de estado (200, 404), encabezados y el contenido (HTML, JSON o texto).

##p1
Mi predicción: En las tres direcciones (`/`, `/hola`, `/lo-que-sea`) el servidor responderá exactamente lo mismo: "Hola desde el servidor". Esto pasa porque la función del servidor no tiene ninguna condición (`if`) que verifique la URL, por lo que siempre ejecuta `res.end()`.
Lo que pasó:(Pruébalo tú mismo en el navegador y complétalo)
Por qué pasó:(Confirma si tu predicción fue correcta)

##p2
Mi predicción: Aparecerán 2 líneas en la terminal por cada carga de página. Una para la ruta solicitada (ej. `/`) y otra automática que hace el navegador buscando el ícono de la pestaña (`/favicon.ico`).
Lo que pasó:(Compáralo mirando la terminal tras cargar la página)
Por qué pasó:(Anota tu conclusión)

##p3
si lo hago con mayuscula o con el slash al final me manda a error 404 como estba configurado

Reflexion 
Hacer un servidor a mano es bastante cansón por tres razones: primero, el enrutamiento es muy frágil porque toca escribir puros if/else y cualquier mayúscula, barra extra o parámetro dinámico rompe todo; segundo, mandar respuestas da pereza porque hay que configurar las cabeceras JSON y convertir los datos a texto manualmente cada vez; y tercero, recibir datos en peticiones POST se vuelve muy canzón al tener que escuchar eventos por pedazos (req.on('data')) para ir pegándolos y procesándolos a mano.