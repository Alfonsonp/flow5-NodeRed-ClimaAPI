# flow5-NodeRed-ClimaAPI
Este repositorio contiene el flow 4 , visto en en los contenidos de Internet de las cosas de Codigo IoT 

# Introducción

Este flow consiste en un tablero que presente la información de temperatura y humedad locales. Este flow recibe la información por MQTT con un broker local.

# Material

- Ubuntu 20.04.
- NodeJS.

# Material de referencia

- Instalación de Virutal Box. 
- Ubuntu 20.04.
- Instalación de NodeRed.
- Introducción a NodeRed.

# Instrucciones

Requisitos previos.

Para que este flow funcione, debes cumplir con los siguientes requisitos previos

 1. Instalación de NodeJS. Se recomienda tener instalado NodeJS en alguna versión LTS. Al momento de creación de este documento, se usó la versión 16.17.0LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM.
 2. Instalación de NodeRed. La instalación se realiza por NPM. Al momento de la creación de este contenido, se usó la versión 3.0.2.
 3. Instalar los nodos node-red-dashboard. Para ello, dirigete a la opcion "Manage Palet" de NodeRed y en la pestaña Install busca node-red-dashboard. Finalmente haz clic en instalar.
 4. Instalación de Broker local Mosquitto MQTT.
 5. Cuenta en OpenWeatherMap.org. Este es el servidor del cual se obtendrán los datos del clima por API.
 6. API Key valida. Deberás generar una API Key con tu cuenta de openweathermaps.org.
 
# Instrucciones de preparación del entorno.
Para ejecutar este flow, es necesario lo siguiente:

 1. Arrancar NodeRed con el comando node-red.
 2. Importar el flow del repositorio.
 3. Coloca tu API Key personal en la API Call del nodo HTTP Request.
 4. Actualiza la IP del broker público.
 5. Hacer clic en el boton Deploy.
# Instrucciones de operación
-Para observar el resutlado de este flow, abre un navegador y dirígete a localhost:1880/ui.
-Para activar las gráficas de clima manual, debes enviar por MQTT un mensaje que contenga un JSON con las variables ID, temp y hum.
# Notas
- La sección manual de este flow se suscribe al tema codigoIoT/fow5/mqtt en un broker local.
- El mensaje mqtt usado para probar este flow es mosquitto_pub -h localhost -t ccodigoIoT/fow5/mqtt -m '{"ID":"Alfonso","temp":25,"hum":58}'
- Para que la gráfica historica muestre información, deben enviarse al menos 2 puntos.
- Para actualizar la IP del broker publico, se recomienda el siguiente comando nslookup broker.hivemq.com. Puedes usar el broker publico de tu elección.
- Para que multiples graficas sean mostradas en la sección de Histórico Público, es necesario que multiples usuarios se encuentren publicando a la vez.


# Resultados
file:///home/alfonso/Im%C3%A1genes/Capturas%20de%20pantalla/Captura%20desde%202022-10-04%2019-48-43.png![image](https://user-images.githubusercontent.com/111294774/193957180-056db9db-2cf2-4355-917d-375eb2acf80f.png)

file:///home/alfonso/Im%C3%A1genes/Capturas%20de%20pantalla/Captura%20desde%202022-10-04%2019-48-54.png![image](https://user-images.githubusercontent.com/111294774/193957297-1bc2abbf-75bd-4a9a-a61d-bfcd170f6bc2.png)

file:///home/alfonso/Im%C3%A1genes/Capturas%20de%20pantalla/Captura%20desde%202022-10-04%2019-49-16.png![image](https://user-images.githubusercontent.com/111294774/193957348-8d74d5e2-fec4-4e66-9952-124320812319.png)



