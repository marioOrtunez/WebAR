# Problemas

A continuación, detallo los problemas que he identificado en Unity para tener un registro futuro:

- [Problema de descompresión de Gzip](#problema-de-descompresión-de-gzip)
- [Problema de pantalla en negro en dispositivos móviles](#problema-de-pantalla-en-negro-en-dispositivos-móviles)

## Problema de descompresión de Gzip

**- Descripción:** Este problema provoca que el proyecto no se cargue correctamente, generando el siguiente mensaje de error:
<p align="center">
<img src="Resources/Mensaje de error del Gzip.png" alt="Mensaje de error del Gzip" style="width:50%;height:50%;">
</p>

**- Solución:** Este inconveniente surge porque, por defecto, **Unity** comprime un archivo *JavaScript* durante el proceso de compilación para *WebGL*. Sin embargo, el servidor web donde se aloja el contenido no está configurado adecuadamente para manejar archivos comprimidos con *gzip*, como es el caso de **Github Pages**.

Para resolverlo, es necesario realizar los siguientes pasos en Unity: 

1. Ir al menú __"File" > "Build Settings" > "Player Settings" > "Publishing Settings" > "Compress Build"__.
2. Cambiar la opción de __Gzip__ por __Disable__.

## Problema de pantalla en negro en dispositivos móviles

**- Descripción:** Este problema ocasiona que, al abrir el proyecto en Android, la pantalla se quede en negro, a pesar de que la cámara esté activa.

**-Solución:** No encontrada.