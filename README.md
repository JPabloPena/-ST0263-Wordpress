# Título
Proyecto 2 - Producto 1

# Autor
Juan Pablo Peña F.

# Software
Wordpress: _Docker_ con _SSL_

# Descripción
Página web básica de _Wordpress_ en _Docker_ con certificado _SSL_ haciendo uso de _NGINX_, montada en _Google Cloud Platform_. 

# Detalles del diseño
1. Se adquirió un dominio de manera gratuita en _freenom.com_.
2. Se desplegó una instancia de _VM_ en _Google Cloud Platform (GCP)_.
3. En _GCP_ se creó una zona en _Cloud DNS_ a la cual se le agregó un conjunto de registro de tipo A con la IP de la instancia y otro registro de tipo CNAME.
4. Se le asignó una IP estática a la instancia.
5. En la instancia se clonó este repositorio en el cual se encuentra la lógica básica de la aplicación.
6. Se desplegó la aplicación en _Docker_.

# Instalación
En _Debian GNU/Linux 10_:

Primero, debemos actualizar el sistema:
```
$ sudo apt-get update
```

Luego, debemos instalar _git_ para clonar el repositorio:
```
$ sudo apt-get install git
```

Posteriormente, debemos instalar _Docker_ y _Docker-Compose_:
```
$ sudo apt-get install docker.io docker-compose
```

Después, debemos clonar este repositorio:
```
$ sudo git clone https://github.com/JPabloPena/ST0263-Wordpress.git
```

Luego, tenemos que ingresar a la carpeta del repositorio (_ST0263-Wordpress_) y después a la carpeta _wordpress_ que se encuentra adentro:
```
$ cd ST0263-Wordpress/
$ cd wordpress/ 
```

Finalmente, debemos ejecutar:
```
$ sudo docker-compose up -d
```

Listo! Ya puede acceder a través de su página web y configurar su sitio _Wordpress_.

# Ejecución
Para acceder solo debe ingresar a alguno de los siguientes enlaces:

www.proyectos-integradores-eafit.tk (Con _SSL_)

proyectos-integradores-eafit.tk (Con _SSL)

Dirección IP: 35.232.147.128
