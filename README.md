# ComposeNginxWordpress
### Vamos a crear un Docker en el cual vamos a instalar Wordpress, phpmyadmin y un servidor de correo con sus correspondientes certificados y firmas.
### El primer paso cambiar y añadir el nombre del dominio y la dirección IP en nuestro equipo el cual podemos encontrar en nuestro archivo host (Ejecutar el bloc de notas como administrador y luego modificar el archivo, no tienes permisos para modificar ese archivo)

```shell
C:\Windows\System32\drivers\etc\host 
```
### Creamos una carpeta en nuestra raíz llamada certs en la cual vamos a insertar nuestros certificados y firmas. En la carpeta nginx y en el archivo wordpres.conf en la línea 13 y 14 del ssl, son las direcciones donde apuntan a los certificados que hemos añadido, podemos modificar esas direcciones a donde tengamos las clave, o podemos poner las claves con el mismo nombre y en la misma dirección a la que apuntan. 

```Shell
.\nginx\wordpres.conf

ssl_certificate           /etc/certs/certificate.pem;
ssl_certificate_key       /etc/certs/certificate-key.pem;
```
