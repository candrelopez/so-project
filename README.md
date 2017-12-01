## Miniproyecto Sistemas Operativos

**Universidad ICESI**  
**Curso:** Sistemas Operativos  
**Docente:** Daniel Barragán C.  
**Tema:**  Servicios web  
**Correo:** daniel.barragan at correo.icesi.edu.co

**Estudiante: A00141804**  
**Nombre: Carlos Andrés Torres López**  

## Objetivos
* Desplegar una aplicación en un servidor que ejecuta el sistema operativo Linux
* Realizar los ajustes y depuración necesarios para desplegar una
aplicación en Linux
* Realizar aplicaciones para obtener información del sistema operativo

## Descripción
Para el despliegue de una aplicación en un servidor se requiere conocer los procedimientos necesarios relacionados con la configuracion de las interfaces de red, ajustes de seguridad, instalación de dependencias, usuarios y herramientas de depuracíon del sistema operativo.

El siguiente proyecto consiste en el despliegue de una aplicación web para obtener información del sistema operativo (La aplicación debe permitir consulta uso de CPU, memoria y espacio en disco). Para este propósito se debe emplear el sistema operativo Ubuntu Server 16.04, el microframework flask y ambientes virtuales.

<p align="center">
  <img src="vista-despliegue.png" alt="webservice architecture"/>
</p>

## Actividades
* Nombre y código de todos los integrantes del grupo (máximo 3) (5%)
* Ortografía y redacción (5%)
* Descripción breve de los pasos para cumplir con lo solicitado
  * Sistema operativo Ubuntu Server 16.04 (10%)
  * Configuración de interfaces de red (10%)
  * Configuración de puertos (10%)
  * Instalación de dependencias (10%)
  * Creación de ambientes virtuales (10%)
  * Aplicación en Python (10%)
  * Validación de la ejecución del servicio (netstat) (10%)
* Pruebas de la solución a través de capturas de pantalla. Puede emplear si lo desea una herramienta de captura de pantalla a formato .gif (10%)
* El informe debe ser entregado en formato pdf a través del moodle y el informe en formato README.md debe ser subido a un repositorio de github. El repositorio de github debe ser un fork de https://github.com/ICESI-Training/so-project y para la entrega deberá hacer un Pull Request (PR) respetando la estructura definida. El código fuente y la url de github deben incluirse en el informe (10%).

## Solución
1. Como primer paso se descargo y se instalo el Ubuntu server desde el link que aparece como referencia.  
Como usuario se configuro un usuaurio Proyecto con la misma contraseña.
2. se procedio a configurar las interfases, en este punto tuve bastantes problemas ya que mi maquina esta configurada bajo una red cerrada y solo funcionaba con iP fija, pero lo solucione trabajando con la red inalambrica. y tuve que deshabilitar el firewall para poder conectarme por ssh. como muestro a continuación y tambien la información de red: 

Firewall:  
<p align="center">
  <img src="firewall.PNG" alt="Install phyton"/>  
</p>  

Configuración de red:  

<p align="center">
  <img src="Config_red.PNG" alt="Install phyton"/>  
</p>  

y asi me pude conectar por SSH :

<p align="center">
  <img src="ssh.PNG" alt="Install phyton"/>  
</p>  

3. Inicialmente se instala el phyton, pero debido a que con la evrsión que instala del phyton tenia problemas, tuve que actualizar la versión del pip (herramienta de phyton que permite instalar dependecias) para que me dejara instalar  el virtualenv, como muestro a continuaciíon:

<p align="center">
  <img src="Actualización phyton.PNG" alt="Install phyton"/>  
</p>  

4.Luego de eso proceso a abrir habilitar los puertos:  

<p align="center">
  <img src="Puertos.PNG" alt="Puertos"/>  
</p>  

5. Luego de esto se instala el virtualenv:  

<p align="center">
  <img src="virtualenv.PNG" alt="Ambiente virtual"/>  
</p>  

6.Luego se crea el ambiente virtual sobre el que se va a trabajar y se va a crear el servicios Web:  

<p align="center">
  <img src="Ambvirtual.PNG" alt="Ambiente virtual"/>  
</p>  

7. y se activa el ambiente virtual:  

<p align="center">
  <img src="activarAmb.PNG" alt="activacion Virtua"/>  
</p>  

8. Luego de esto se instala la dependencia del flask para montar el servicio web :  

<p align="center">
  <img src="Install faslk.PNG" alt="activacion Virtua"/>  
</p>  


9. Luego de esto se debe crear un script.py que es el que va a contener el codigo que va a entregar la información del sistema por medio del servicio web, el nombre que le puse al script es servicio.py, a continuación muestro el contenido del archivo:  

<p align="center">
  <img src="script_py.PNG" alt="activacion Virtua"/>  
</p>  

 10.Luego inicio el servicio ejecutando el script servicio.py que contiene el codigo de la imagen anterior:  
 
 <p align="center">
  <img src="correr_servicio.PNG" alt="activacion Virtua"/>  
</p>  
 
 
## Referencias  

* https://www.ubuntu.com/download/server
