# Título
Proyecto 2

# Autor
Juan Pablo Peña F.

# Software
Wordpress: _Docker_

# Descripción


# Detalles del diseño


# Instalación
En _Ubuntu_:

Primero debemos actualizar el sistema:
```
$ apt update
```

Luego debemos instalar _docker_:
```
$ apt install docker.io docker-compose
```

# Ejecución
## Cliente (_publisher.py_)
Para ejecutar el cliente debe:
```
$ python3 publisher.py <ip-server> <port>
```
El _ip-server_ y _port_ son del servidor de _RabbitMQ_. Ejemplo, para conectarse con mi _RabbitMQ_:

_ip-server:_ 34.226.36.159

_port:_ 5672
```
$ python3 publisher.py 34.226.36.159 5672
```
Luego, al ejecutar se le pedirá el usuario y contraseña de RabbitMQ, que para el laboratorio 4 son _user_ y _password_ respectivamente:
```
Usuario de RabbitMQ:
 >user
Contraseña de RabbitMQ:
 >password
```
Después, se le pedirá un usuario y un email en los cuales puede poner lo que desee:
```
 [x] Escriba su nombre de usuario:
 >prueba123
 
 [x] Escriba su email:
 >prueba@prueba.com
```
Finalmente, podrá enviar tareas a la cola escribiendo únicamente un número como se indica en la aplicación.

## Servidor (_subscriber.py_)
Para ejecutar el servidor debe:
```
$ python3 subscriber.py <ip-server> <port>
```
El _ip-server_ y _port_ son del servidor de _RabbitMQ_. Ejemplo, para conectarse con mi _RabbitMQ_:

_ip-server:_ 34.226.36.159

_port:_ 5672
```
$ python3 subscriber.py 34.226.36.159 5672
```
Luego, al ejecutar se le pedirá el usuario y contraseña de RabbitMQ, que para el laboratorio 4 son _user_ y _password_ respectivamente:
```
Usuario de RabbitMQ:
 >user
Contraseña de RabbitMQ:
 >password
```
Finalmente, el servidor ejecutará automáticamente todas las tareas que se encuentren en la cola.
