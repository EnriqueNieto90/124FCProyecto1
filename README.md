# Fundamentos de contenerización
## Actividad 1. Servidor Web Simple con Nginx

Paso 1. Construir la imagen con el mismo nombre que el repositorio con la versión 1.0
```
sudo docker image build --tag 124fcproyecto1:1.0 .
```
- Comprobar que se ha creado la imagen:
```
sudo docker image ls
```
- Borrar imagen:
```
sudo docker image rmi --force 124FCProyecto1
```
	
Paso 2. Ejecutar el contenedor en el puerto 80
```
docker container run -d -p 80:80 --name 124FCProyecto1 124fcproyecto1:1.0
```
- Comprobar que se ha ejecutado el contenedor
```
sudo docker container ls
```
- Borrar contenedor (prueba)
```
sudo docker container rm --force 124FPCroyecto1
```

Paso 3. Comprobación: http://localhost
	
Paso 4. Se pide modificar el fichero index.html desde el contenedor
- Acceder al bash del contenedor en ejecución:
```
sudo docker exec -it 124FCProyecto1 bash
```
- Entrar en el contenedor
```
cd /usr/share/nginx/html
```
- Modificar el index con el editor nano, guardar y salir. Comprobación: http://localhost
```
nano index.html
```
- 
