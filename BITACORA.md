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
si lo hago con mayuscula o con el slash al final me manda a error 404 como estaba configurado

Reflexion 
Hacer un servidor a mano es bastante cansón por tres razones: primero, el enrutamiento es muy frágil porque toca escribir puros if/else y cualquier mayúscula, barra extra o parámetro dinámico rompe todo; segundo, mandar respuestas da pereza porque hay que configurar las cabeceras JSON y convertir los datos a texto manualmente cada vez; y tercero, recibir datos en peticiones POST se vuelve muy canzón al tener que escuchar eventos por pedazos (req.on('data')) para ir pegándolos y procesándolos a mano.

##p4
al ingresar/no-existe saldra error 404

reflexion m2
1.aveces no se ejecutaba el servidor
2.el script del package toco modificarlos
3.casi no puede ejecutar el server
 
##p5
en el navegador se quedara en bucle
en la terminal e imprimirá la línea del registro (hora, método y URL) una sola vez al entrar la petición, pero ahí se detendrá la ejecución del servidor para esa solicitud 

##p 6
Código de estado: 200 OK.
Body: Muestra nada porque el sistema compara el número 1 del arreglo con el texto "1" de la URL y no encuentra ninguna coincidencia.
el 1 aparece sin comillas

##p7
Recibe el estado 404 Not Found con el mensaje de que la actividad no existe.
En la terminal: Muestra un error grave indicando que el servidor intentó enviar dos respuestas para una misma petición.
El return es obligatorio para cortar la ejecución e impedir que el código siga de largo hasta el res.json(actividad).