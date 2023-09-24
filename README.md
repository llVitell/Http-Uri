# Actividad: Introducción a HTTP y URI
## Pregunta 1

¿Cuáles son las dos diferencias principales que has visto anteriormente y lo que ves en un navegador web 'normal'? ¿Qué explica estas diferencias?
- Vista local
![](Imagenes/saasbookLocal.jpg)
- Vista Web
![](Imagenes/saasbookWeb.jpg)

### Respuesta 
- La imagen no se muestra: Se debe a qué el llamado de la misma es através de una ruta, tendriamos que tener la imagen descargada para que se visualize.
- El texto no es el mismo: Esto es por la misma configuración de la página la cual muestra un texto distinto cada que se actualiza.

## Pregunta 2
Suponiendo que estás ejecutando curl desde otro shell ¿qué URL tendrás que pasarle a curl para intentar acceder a tu servidor falso y por qué?

### Respuesta 
Segun el comando `ncat -1 8081` se está escuchando el puerto 8081 entonces para acceder a este servidor debemos usar:
```Shell
curl localhost:8081
```

## Pregunta 3
La primera línea de la solicitud identifica qué URL desea recuperar el cliente. ¿Por qué no ves http://localhost:8081 en ninguna parte de esa línea?
```Shell
C:\Users\viteo>ncat -l 8081
GET / HTTP/1.1
Host: localhost:8081
User-Agent: curl/8.0.1
Accept: */*
```
### Respuesta
La razón es que la solicitud HTTP enviada por curl solo contiene la ruta relativa en lugar de la URL completa
## Pregunta 4
Según los encabezados del servidor, ¿cuál es el código de respuesta HTTP del servidor que indica el estado de la solicitud del cliente y qué versión del protocolo HTTP utilizó el servidor para responder al cliente?

```Shell
HTTP/1.1 200 OK
Connection: keep-alive
Content-Type: text/html;charset=utf-8
Content-Length: 480
X-Xss-Protection: 1; mode=block
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
Server: WEBrick/1.4.2 (Ruby/2.6.6/2020-03-31)
Date: Sun, 24 Sep 2023 18:38:16 GMT
Via: 1.1 vegur

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1" crossorigin="anonymous">
    <title>Random Word Generator</title>
  <body class="container">
    <div id="image">
      <img src="esaas.png">
    </div>
    <div id="word">
      injure
    </div>
  </body>
</html>
```
### Respuesta





