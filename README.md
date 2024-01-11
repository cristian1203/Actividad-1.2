#  Sitio Local en Jekyll con Dockers
## Paso 1: Instalar Docker y comprabar que esta instalado
Primero, necesitará Docker instalado en su máquina local. Docker Community Edition es gratuito y fácil de instalar.
Siga las instrucciones de su sistema operativo y luego asegúrese de que Docker se esté ejecutando, para ello ejecutaremos el comando dockers hello-world.
![image](https://github.com/cristian1203/Actividad-1.2/assets/151034282/568a0701-4d4c-49c4-a341-cc95612445ba)  
## Paso 2: Creación de un contenedor Docker con Jekyll 
Con Docker instalado, puedes usarlo desde la línea de comando. Abra su terminal y navegue hasta el directorio vacío donde desea crear su sitio Jekyll.  
 ```
docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll
```
![image](https://github.com/cristian1203/Actividad-1.2/assets/151034282/19679ce2-87f0-4dd3-b804-054403ea005d)
## Paso 3 Ahor crearemos nuestro blog   
 ```
docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll new blog
```
![image](https://github.com/cristian1203/Actividad-1.2/assets/151034282/58b695d8-1e4c-4367-986b-fded9285e4a7)  
## Paso 4 Ahora generamos  un sitio HTML estático a partir del contenido del proyecto jekyll
 ```
docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll bash -c "bundle install"
```
![image](https://github.com/cristian1203/Actividad-1.2/assets/151034282/6fadccf1-604f-4f05-9320-71fdc1acc2de)

## Paso 5 Este comando nos permite servir de forma local un sitio HTML estático generado a partir del contenido del proyecto Jekyll.  
 ```
docker run -it --rm -p 4000:4000 -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll serve --force_polling
```
![image](https://github.com/cristian1203/Actividad-1.2/assets/151034282/582976aa-55a9-4ee3-83ae-31d0e5851ef6)

## Paso 6 Una vez arrancado ya el servidor jekyll solo tendremos que buscar nuestra web jekyll con la siguiente ip.  
![image](https://github.com/cristian1203/Actividad-1.2/assets/151034282/a9068f14-f81e-4d0a-a456-7e8879863662)  
![image](https://github.com/cristian1203/Actividad-1.2/assets/151034282/fcefc03d-e6f1-424b-8a79-d4033ddf2961)






