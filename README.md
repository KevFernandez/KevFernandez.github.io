# KevFernandez.github.io

            
 
SOLARBLIND 

 

 ![WhatsApp Image 2024-11-23 at 15 30 25](https://github.com/user-attachments/assets/6a8c1751-376c-43c7-9275-f53cfb5fedf7)


 

 

Este proyecto tiene como propósito diseñar e implementar un sistema automatizado para cortinas que se ajuste automáticamente en función de la intensidad de la luz solar. La idea central es combinar tecnologías modernas para ofrecer una solución que mejore el confort, la eficiencia energética y la comodidad del usuario en espacios interiores. Al integrar un sensor de luz, motores controlados electrónicamente y un sistema de iluminación inteligente, el proyecto busca optimizar el uso de la luz natural y reducir la dependencia de iluminación artificial, contribuyendo a un entorno más sostenible. 

_____________________________________________________________ 

 

Índice 

    Introducción 

     sistema de cortina automática 

    ¿Cómo funciona? 

    Monitoreo continuo de luz solar 

    Procesamiento inteligente 

    Movimiento automático de la cortina 

    Iluminación artificial complementaria 

    Beneficios clave 

    Comodidad total 

    Ahorro de energía 

    Integración inteligente 

    Adaptable a tus necesidades 

    Tecnología detrás del sistema 

    ESP32 

    Sensor de luz (LDR) 

    Motor a pasos + Driver ULN2003 

    Focos inteligentes y dimmer 

 

    Conexiones esquematicas y  pcbs 

      a. Conexiones del esquematico 

      b. Placa principal 

      c. Placa controladora de luz 

 

      6. Codigo y conexiones 

                 a. Explicacion del codigo 

                  

 

 

¿Qué es nuestro sistema de cortina automática? 

Se trata de una solución innovadora que combina tecnología avanzada con funcionalidad práctica. Mediante sensores de luz, motores precisos y un sistema de iluminación inteligente, nuestra cortina automática se adapta a las condiciones de iluminación natural para garantizar comodidad, ahorro de energía y una experiencia personalizada. 

 

¿Cómo funciona? 

Nuestro sistema opera de manera completamente automática. Aquí te contamos cómo: 

    Monitoreo continuo de luz solar: Un sensor de luz detecta los niveles de iluminación exterior. 

    Procesamiento inteligente: Un ESP32, el cerebro del sistema, analiza los datos del sensor y toma decisiones en tiempo real. 

    Movimiento automático de la cortina: Un motor a pasos, controlado por un driver de alta precisión, ajusta la posición de la cortina según las necesidades del momento. 

    Iluminación artificial complementaria: Cuando la luz natural no es suficiente, nuestros focos inteligentes y un dimmer se activan automáticamente para mantener un ambiente luminoso y acogedor. 

 

Beneficios clave 

✅ Comodidad total: Disfruta de un espacio siempre bien iluminado, sin preocuparte por abrir o cerrar cortinas manualmente. 

✅ Ahorro de energía: Optimizar el uso de luz natural, reduciendo el consumo eléctrico. 

✅ Integración inteligente: Combina luz solar y artificial para crear el ambiente perfecto en cada momento del día. 

✅ Adaptable a tus necesidades: Ideal para hogares, oficinas o cualquier espacio que requiera una gestión eficiente de la luz. 

 

Tecnología detrás del sistema 

    ESP32: Procesa datos y toma decisiones en tiempo real. 

    Sensor de luz (LDR): Mide la intensidad de la luz solar. 

    Motor a pasos + Driver ULN2003: Control preciso del movimiento de la cortina. 

    Focos inteligentes: Ajustar la iluminación artificial según las condiciones del entorno. 

_____________________________________________________________ 

 

Conexiones esquematicas y pcbs 

 

 

Placa principal:  

 

 

 ![WhatsApp Image 2024-11-23 at 15 06 55](https://github.com/user-attachments/assets/7bc9c963-7966-40f7-a42c-5d8625eda1b3)


 ![WhatsApp Image 2024-11-23 at 15 06 56](https://github.com/user-attachments/assets/9e304cf3-d5e1-4eb3-bcef-529ca9931a1b)


Placa controladora de luz: 

 

 

 ![CONTROLADORDELUZ](https://github.com/user-attachments/assets/0a6a7751-5750-4f0c-8cab-d2b45f7c7ec5)


 

 ![pcbluz](https://github.com/user-attachments/assets/f73f357a-4d4d-4d52-8c9d-412f03ebb4a5)


_________________________________________________________________________________ 

Codigos y conexiones 

 

![elcodigo](https://github.com/user-attachments/assets/0e64fabc-33c1-4ca1-85ba-17e4d0b82156)

 

Explicacion del código 

El código para el sistema de cortina automática está diseñado para controlar un motor paso a paso que ajusta la posición de la cortina según los niveles de luz detectados por un sensor LDR. Este código emplea la librería stepper.h para gestionar el motor, facilitando su operación en pasos específicos para movimientos precisos. 

Estructura del Código 

    Declaraciones Iniciales: 

    Se define la constante pasosPorVuelta para determinar los pasos necesarios para una vuelta completa del motor, lo que permite controlarlo con precisión. 

    Se asignan los pines GPIO 34, 35, 32 y 33 del ESP32 para conectar el driver del motor, asegurando la comunicación entre el microcontrolador y el motor. 

    Configuración Inicial (void setup): 

    Se establece la velocidad de transmisión de datos con Serial.begin(115200), necesaria para la comunicación entre el ESP32 y el ordenador. 

    La velocidad del motor se ajusta con motor.setSpeed, utilizando la función de la librería stepper.h. 

    Se configura el pin del ESP32 que recibe los datos analógicos del sensor LDR, ya que este entrega valores en un rango continuo (0-4500), incompatible con señales digitales. 

    Bucle Principal (void loop): 

    El sistema opera en un ciclo continuo para monitorear la intensidad de la luz solar. 

    Se utiliza analogRead para leer los valores del sensor y Serial.println para verificar su funcionamiento mediante el Serial Monitor. 

    Con la estructura condicional if, se determina el comportamiento del motor: 

    Mayor a 3000: Alta intensidad de luz; el motor gira en sentido horario para bajar la cortina. 

    Entre 1500 y 3000: Luz baja o media; el motor gira en sentido antihorario para subir la cortina. 

    Menor a 1500: Baja intensidad de luz; el motor permanece inactivo. 

    Verificación y Optimización: 

    Se utilizan Serial.println dentro de las condiciones para verificar las acciones del motor en función de los valores del sensor. 

    Se incluye un delay(500) para que el bucle se repita cada 500 ms, proporcionando tiempo suficiente para procesar los datos y ejecutar las acciones necesarias. 

Resumen del Funcionamiento 

El código asegura que la cortina se ajuste automáticamente según la luz ambiental. Cuando la luz es intensa, el motor baja la cortina, mientras que con luz media o baja, la sube. Si hay poca o ninguna luz, el sistema permanece inactivo. Este enfoque garantiza un control preciso y eficiente del sistema, manteniendo el confort del usuario y optimizando el uso de la luz natural. 
 
