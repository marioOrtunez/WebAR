# Problemas

A continuación, detallo los problemas que he identificado en Unity para tener un registro futuro:

- [Problema de descompresión de Gzip](#problema-de-descompresión-de-gzip)
- [Problema de configuración de la descarga de los archivos Wasm](#problema-de-configuración-de-la-descarga-de-los-archivos-wasm)
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

## Problema de configuración de los archivos Wasm

**- Descripción:** Este problema sucedió al instalar e implementar el *URP (Universal Render Pipeline)* en el proyecto, sacando dos errores, uno en el buscador y otro en el proyecto, mostrados en esta imagen (imagen sacada desde el buscador **Firefox**):

<p align="center">
<img src="Resources/Mensajes de error del Wasm.png" alt="Mensajes de error del Wasm" style="width:50%;height:50%;">
</p>

**- Solución:** Este error esta probocado por un fallo en el archivo **"Build" > "Build.wasm"** (nombre del archivo depende del nombre que le pongas al build), asi que seria revisarlo. 

## Problema de pantalla en negro en dispositivos móviles

**- Descripción:** Este problema ocasiona que, al abrir el proyecto en Android, la pantalla se quede en negro, a pesar de que la cámara esté activa.

**-Solución:** Por ahora la solución esta en cambiar el **Scriptable Render Pipeline Settings** que se encuentra en **"Project Settings" > "Graphics"**, añadiendo un **URP (Universal Render Pipeline)**, configurandolo para la ocasión.
Esta solución es provisional, debido a que todavía se queda en algunos momentos en negro la pantalla. 