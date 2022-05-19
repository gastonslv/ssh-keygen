### Cómo Crear tu llave SSH

Primero que nada, hay que asegurarse de que no tenes una. Por defecto, el directorio con la llave
está en ´~/.ssh´. Podes verificarlo de la siguiente manera:


```
$> cd ~/.ssh
$> ls
 authorized_keys2  id_dsa       known_hosts
 config            id_dsa.pub
```

Acá lo que importa es id_dsa (o tambien id_rsa) y id_dsa.pub (id_rsa.pub). El archivo que termina
en ``.pub`` es tu calve pública, y el otro archivo es tu clave privada. Si no tenés esos archivos,
entonces vamos a crearlos.


