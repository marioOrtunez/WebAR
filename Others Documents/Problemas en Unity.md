# Problemas Unity
Estos son los problemas que me estoy encontrando en __Unity__ para tenerlos a mano en un fututo:
- [Problema de descompresion de Gzip.](#problema-de-descompresion-de-gzip)
- [Problema de pantalla en negro del movil](#problema-de-pantalla-en-negro-del-movil)

## Problema de descompresion de Gzip
Este problema se da debido a que de manera predeterminada __Unity__, comprime un archivo JavaScript durante el proceso de compilación para WebGL, pero servidor web donde estás alojando tu contenido no está configurado correctamente para manejar archivos comprimidos con gzip (en este caso __Github Pages__). Por lo que al ejecutar en el navegador web se mostrara este error:

<p align="center">
<img src="Resources/Mensaje de error del Gzip.png" alt="Mensaje de error del Gzip" style="width:50%;height:50%;">
</p>

Para solucionarlo tendremos que ir a __Unity__ y entrar en nuestro proyecto, despues entrar en __"File" > "Build Settings" > "Player Settings" > "Publishing Settings" > "Compress Build"__ y cambiar la eleccion de __Gzip__ por __Disable__. 

## Problema de pantalla en negro del movil
 (Por ahora sin solucion)