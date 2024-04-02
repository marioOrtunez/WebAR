# URP

**URP o Universal Render Pipeline** es la solución que encontré para el problema de la pantalla en negro del móvil. Este problema está provocado por problemas de compatibilidad, más explicado [aquí](PROBLEMS.md#problema-de-pantalla-en-negro-en-dispositivos-móviles).

>## Definición
>**URP (Universal Render Pipeline)** es un sistema de renderizado en **Unity** que equilibra rendimiento y calidad visual. Ofrece personalización, alto rendimiento en diversas plataformas, facilidad de uso y compatibilidad con shaders. Es ideal para proyectos que requieren eficiencia y flexibilidad en el renderizado.

## Instalación
Para instalar **URP** en nuestro proyecto seguiremos los siguientes pasos:
- Descargamos el plugin llamado **Universal RP** desde **"Window" > "Package manager"**, y aquí seleccionamos arriba **Unity Registry**, lo buscamos y lo instalamos.
- Creamos los archivos de Assets del **URP**, tenemos para crearlo con **"Click derecho" > "Create" > "Rendering" > "URP Asset" (2D o Universal según necesitemos)**.
- Lo añadimos a **Scriptable Render Pipeline Settings** desde **"Edit" > "Projects Settings" > "Graphics"**, cambiando por el None por el **URP**.

## Configuración
La configuración que mejor me fue, es:
 - **Desabilitar HDR**, el cual suma puntos a que le cueste proecesar al dispositivo.