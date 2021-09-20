# Título
Proyecto 2

# Autor
Juan Pablo Peña F.

# Software
Wordpress: _Docker_

# Descripción


# Detalles del diseño


# Instalación
En _Debian GNU/Linux 10_:

Primero debemos actualizar el sistema:
```
$ sudo apt update
```

Luego debemos instalar _docker_:
```
$ sudo apt install docker.io docker-compose
```

Ir a la carpeta _opt_:
```
$ cd /opt/
```

Crear una carpeta con el nombre de _wordpress_:
```
$ sudo mkdir wordpress
```

Entrar a la carpeta y crear el siguiente fichero:
```
$ cd wordpress/
$ sudo nano docker-compose.yml
```

Dentro, copiar el código que se encuentra en el siguiente link: () guardamos (Ctrl + o) y salimos (Ctrl + x).

Luego debemos ejecutar:
```
$ sudo docker-compose up -d
```

Finalmente debemos hacer:
```
$ sudo docker logs wordpress_wordpress_1
$ sudo docker logs wordpress_db_1
```

```
$ sudo apt install certbot
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
