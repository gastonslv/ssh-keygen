### Cómo Crear tu llave SSH 🔑

Primero que nada, hay que asegurarse de que no tenes una. Por defecto, el directorio 📁 con la llave
está en ``~/.ssh``. Podes verificarlo de la siguiente manera:


```
$> cd ~/.ssh
$> ls
authorized_keys2  id_dsa       known_hosts
config            id_dsa.pub
```

Acá lo que importa es id_dsa (tambien puede estar como id_rsa) e id_dsa.pub (id_rsa.pub). El archivo que termina
en ``.pub`` es tu clave pública, y el otro archivo es tu clave privada. Si no tenés esos archivos,
entonces vamos a crearlos.

Para crear la llave, vamos a utilizar el programa ``ssh-keygen``, que por lo general ya viene incluido en el paquete SSH de los sistemas Linux/Mac o en el paquete MSysGit en los sistemas Windows:
Ejecutamos el programa:

```
$> ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/home/schacon/.ssh/id_rsa):
```
En esta parte, el programa nos pide que ingresemos la ubicación donde queremos guardar la carpeta ``.ssh/id_rsa``. Si damos enter sin aclarar nada, se va a guardar en $HOME (es lo recomendable).

```
Created directory '/home/schacon/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
```
Luego, donde dice ``Enter passphrase:`` tenemos que poner una contrasña (si se deja vacío, no tendra clave la llave). Esta contraseña debe repetirse tal cual en ``Enter same passphrase again:``.

```
Your identification has been saved in /home/schacon/.ssh/id_rsa.
Your public key has been saved in /home/schacon/.ssh/id_rsa.pub.
The key fingerprint is:
d0:82:24:8e:d7:f1:bb:9b:33:53:96:93:49:da:9b:e3 schacon@mylaptop.local
```
Ya esta lista tu clave.
***
Toda esta información está en [4.3 Git en el Servidor - Generando tu clave pública SSH](https://git-scm.com/book/es/v2/Git-en-el-Servidor-Generando-tu-clave-p%C3%BAblica-SSH)



