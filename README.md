Para configurar tanto el servidor como el cliente ubuntu hay que seguir los siguientes paso:
1. Crear una máquina desktop (puigcastellar1) y desde donde lanzaras los scripts y crear el server (puigcastellar1 y personal1).
2. Copiar el enlace raw de ansibles.zip que está en este mismo repositorio.
3. En la máquina desde donde lanzamos el ansible descargamos el archivo zip con el siguiente comando: wget https://github.com/HJMsmx2/ansibles/raw/refs/heads/main/ansibles.zip.
4. Después descomprimimos la carpeta con este comando: unzip ansibles.zip.
5. Luego lanzamos el script con: bash configurar_server.sh (ip del server enp1s0).
6. Cuando el script haya acabado encendemos el cliente ubuntu (personal1) y comprobamos si tiene acceso a internet y la ip que le corresponde (192.168.1.3).
7. Teniendo encendidas las tres máquinas lanzamos el script con el comando: bash configurar_cliente.sh.
Una vez configurado el server y el cliente ubuntu podemos apagar tanto la máquina desde donde hemos lanzado el ansible como la cliente ubuntu dejando solo encendida el server.

Para conectar el windows (personal1) al AD CD que hemos creado anteriormente con el script en la máquina server:
1. Encendemos la máquina windows y comprobamos que el Kea de la máquina server le haya dado una ip
2. Entramos en Obtener acceso a trabajo o escuela
3. Le damos a conectar que aparecerá y dentro accedemos a añadir un nuevo AD CD.
4. Ponemos nuestro dominio (hjm)
5. Luego nos pedirán el usuario (administrator) y contraseña (usuario1234*).
6. Reiniciamos la máquina windows y ya podremos acceder a la cuenta AD CD con la sesión del usuario y contraseña del punto anterior.

En caso de que no podamos acceder con el Kea tendremos que poner manualmente la ip fija:
1. En configuración entramos en el apartado de ethernet y a cambiar opciones del adaptador
2. Entramos en la instancia de ethernet que tenemos y le damos a propiedades
3. Seleccionamos Protocolo de internet versión 4
4. Y luego ponemos los siguientes datos: la ip que le corresponde a esa máquina, en puerta de enlace predeterminada ponemos 192.168.1.2 y en dns ponemos 192.168.1.2
   



