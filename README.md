# KevFernandez.github.io

3- Objetivo del Proyecto 

  

El objetivo principal de este proyecto es desarrollar una cortina automatizada sensible a la luz solar, capaz de ajustarse automáticamente según la intensidad de luz del ambiente. Este sistema pretende mejorar la eficiencia energética en espacios interiores al controlar la entrada de luz solar, optimizando así la regulación de la temperatura y la iluminación natural. La cortina automática busca también aumentar la comodidad de los usuarios al reducir la necesidad de ajustar manualmente el sistema de cortinas a lo largo del día. De esta manera, el proyecto contribuye tanto a la sostenibilidad energética como al confort personal, con un enfoque en el aprovechamiento de tecnología accesible y de bajo costo. 

  

Este sistema de cortina está diseñado para reaccionar automáticamente ante los cambios de luz solar. Utilizando sensores de luz, se detecta la intensidad luminosa en el entorno; con esta información, el sistema ajusta la posición de la cortina en función de los niveles de luz. Durante el día, por ejemplo, si la intensidad de luz solar alcanza un nivel alto, el sistema bajará la cortina para bloquear parte de la luz y proteger el ambiente interior del exceso de calor o de luz directa. En cambio, en momentos de luz moderada o baja, el sistema permitirá que la cortina suba y deje entrar más luz natural, lo que reduce el uso de iluminación artificial. 

 

4-*IMAGEN DEL PROYECTO*  

 

5-Automatización y Teoría de Control 

La automatización se basa en la aplicación de sistemas automáticos para realizar tareas sin intervención humana. En este proyecto, se aplica la teoría de control para programar la respuesta automática de la cortina ante cambios de luz detectados por los sensores. La teoría de control estudia la forma en que se regulan las variables dentro de un sistema para mantenerlo en un estado deseado. En este caso, el control implica un sistema de retroalimentación entre el sensor de luz y el motor que sube o baja la cortina, manteniendo el ambiente con el nivel de luz óptimo. 

  

Microcontroladores y Electrónica 

La teoría de microcontroladores se centra en el funcionamiento de pequeños sistemas de procesamiento, como el Arduino o Raspberry Pi, que se utilizan para recibir datos de los sensores y controlar el motor de la cortina. Un microcontrolador es un dispositivo integrado capaz de ejecutar órdenes de programación y tomar decisiones en tiempo real. En este proyecto, el microcontrolador recibe señales del sensor de luz y, en función de la programación que se le haya dado, decide si debe accionar el motor para mover la cortina. La electrónica aplicada aquí se basa en circuitos de control de bajo consumo que optimizan la respuesta del sistema a los niveles de luz. 

 

    12)  

    COMPONENTES/PRECIOS 

    ESP32; 16300$ 

    Stepper motor + driver unl 2003 Arduino 8600; 8700$ 

    Sensor de Luz; 5400$ 

    Placa; 8000$  

    Pineras; 1500$ 

    Cables dupont; 11650$ 

    Resistencias; 1000$ 

    Borneas; 4290$ 

    Foco inteligente; 8000 

    Dimmer; 6000 

    Precio total; 70,740 

6)   

 

Capítulo 1: Introducción 

Contexto 

Actualmente, la tecnología de automatización y domótica está transformando los hogares y edificios al proporcionar herramientas que aumentan la eficiencia energética, la comodidad y el control sobre los recursos. La automatización de elementos como la iluminación, el aire acondicionado y las cortinas representa un avance significativo para optimizar el uso de la energía, reducir el impacto ambiental y mejorar la calidad de vida de los usuarios. La presente propuesta de una cortina automática controlada por la intensidad de la luz solar responde a una necesidad práctica y sostenible. 

Problema 

Uno de los problemas comunes en espacios interiores es la falta de un control eficiente de la luz natural. Sin una adecuada gestión de la entrada de luz solar, los espacios pueden calentarse excesivamente o quedarse con poca luz, lo que afecta tanto el consumo de energía (a través de la climatización y la iluminación artificial) como el confort visual de los ocupantes. El uso de sistemas de cortinas automatizadas permite regular la luz natural que entra en un espacio, lo que ayuda a equilibrar la temperatura interior y a reducir el uso de luces artificiales, contribuyendo al ahorro energético y a una mejor calidad de vida. 

Objetivo General 

El objetivo principal de este proyecto es desarrollar una cortina automática sensible a la luz solar, capaz de ajustar su posición según los niveles de luz en el ambiente. Este sistema pretende mejorar la eficiencia energética, aumentar la comodidad del usuario y optimizar el uso de la luz natural en espacios interiores. 

Objetivos Específicos 

    Implementar un sensor de luz que detecte de manera precisa la intensidad luminosa en el entorno. 

    Programar un microcontrolador (ESP32) que reciba datos del sensor de luz y controle el motor de la cortina de manera automática. 

    Integrar el sistema de cortinas con focos inteligentes y un dimmer para lograr un control completo de la iluminación. 

    Probar el sistema en diferentes condiciones de luz para garantizar su funcionalidad y efectividad. 

Justificación 

Este proyecto es relevante tanto para la eficiencia energética como para la comodidad del usuario. Al ajustar automáticamente la cortina según la luz natural disponible, se puede reducir el uso de energía para iluminación artificial y climatización, logrando un hogar más sostenible y amigable con el medio ambiente. Además, la automatización contribuye al confort, evitando que los usuarios tengan que realizar ajustes manuales en la cortina a lo largo del día. 

 

Capítulo 2: Marco Teórico 

Para la implementación de una cortina automatizada controlada por luz solar, es fundamental entender los conceptos teóricos que respaldan el funcionamiento de cada componente y los principios de automatización. En este capítulo, se exploran los conceptos clave que sustentan el diseño y la operación del sistema. 

1. Fundamentos de la Óptica y Comportamiento de la Luz Solar 

La óptica es la rama de la física que estudia el comportamiento y las propiedades de la luz. En este proyecto, los principios de la fotometría, una subdisciplina de la óptica que se centra en medir la luz visible para el ojo humano, son esenciales. Estos estudios permiten comprender cómo la luz solar incide y varía en intensidad según factores como la posición del sol, el clima y las estaciones del año. La teoría fotométrica, en particular, ayuda a determinar el umbral adecuado de luz para que el sistema de cortina automática opere de manera efectiva, abriendo la cortina cuando la luz natural es insuficiente y cerrándola cuando la intensidad de la luz es alta para reducir el calor y el brillo excesivo. 

2. Teoría de Sensores de Luz (Fotoceldas y LDRs) 

Los sensores de luz utilizados en el proyecto, como los fotodiodos o resistores dependientes de la luz (LDR), funcionan en base al principio de fotoconductividad, donde ciertos materiales aumentan su conductividad eléctrica en presencia de luz. Este principio es fundamental en dispositivos que responden automáticamente a la intensidad de luz. En el sistema de cortina automática, los sensores de luz medirán continuamente la luminosidad ambiental y enviarán estos datos al microcontrolador para determinar cuándo debe moverse la cortina. La teoría detrás de los sensores LDR establece que, a medida que la luz incide en el sensor, su resistencia disminuye, permitiendo que el sistema detecte variaciones en la luz y ajuste la cortina en consecuencia. 

3. Automatización y Teoría de Control 

La teoría de control es esencial en sistemas automatizados. En este proyecto, el control automático de la cortina se basa en un sistema de retroalimentación: el sensor de luz mide la intensidad luminosa, y el microcontrolador, programado con ciertos umbrales, controla el motor de la cortina en función de estos valores. La teoría de control estudia cómo mantener una variable dentro de un rango deseado mediante ajustes automáticos, y en este caso, el objetivo es mantener la cantidad de luz natural en el espacio en un nivel cómodo. Un sistema de retroalimentación permite que el microcontrolador ajuste la cortina en tiempo real sin intervención manual, asegurando un control continuo y preciso. 

4. Microcontroladores y Electrónica 

La teoría de microcontroladores se centra en el funcionamiento de estos sistemas de procesamiento compacto, como el ESP32, que se utiliza en este proyecto. Los microcontroladores son dispositivos programables capaces de ejecutar órdenes y tomar decisiones basadas en datos de entrada, como los niveles de luz detectados. En el caso de la cortina automática, el ESP32 recibe señales del sensor de luz, y con base en una lógica programada, decide cuándo y en qué dirección debe moverse el motor. Además, la teoría de electrónica aplicada permite diseñar circuitos de baja potencia que optimizan el consumo energético del sistema. 

5. Eficiencia Energética y Sostenibilidad 

El ahorro de energía es uno de los principales objetivos de la automatización en entornos interiores. Diversos estudios sobre eficiencia energética destacan que el control adecuado de la luz natural reduce el uso de iluminación artificial y climatización, lo que se traduce en una disminución del consumo eléctrico. Los principios de sostenibilidad buscan aprovechar al máximo los recursos naturales disponibles, como la luz solar, para reducir la dependencia de fuentes de energía artificiales. En este proyecto, al regular la entrada de luz solar con una cortina automatizada, se contribuye a un ambiente más eficiente energéticamente y menos contaminante, alineado con los objetivos de sostenibilidad y responsabilidad ambiental. 

6. Integración de Sistemas Domóticos 

La domótica, o automatización del hogar, busca integrar sistemas de control en el entorno doméstico para aumentar el confort, la seguridad y la eficiencia. Este proyecto de cortina automática representa una aplicación domótica al controlar la luz solar que entra en una habitación sin intervención humana. La teoría de domótica estudia cómo diferentes dispositivos (en este caso, la cortina, el sensor de luz y la iluminación inteligente) se comunican entre sí para mejorar la experiencia del usuario y optimizar el uso de recursos. La integración con focos inteligentes y dimmers permite un sistema de iluminación integral, donde tanto la luz natural como la artificial se regulan automáticamente para mantener un ambiente óptimo. 

7. Diseño de Interfaces de Usuario (UI) y Experiencia de Usuario (UX) 

En un sistema automatizado, es importante considerar cómo los usuarios interactúan con el dispositivo. Si bien el objetivo es minimizar la intervención manual, el diseño de interfaces de usuario (UI) y la experiencia de usuario (UX) son esenciales si se planea ofrecer una aplicación o control remoto. Los principios de UX/UI se enfocan en hacer que la tecnología sea intuitiva y accesible para el usuario, asegurando que cualquier ajuste manual que desee realizar sea sencillo y directo. Una interfaz clara y funcional facilita la adopción del sistema y mejora la satisfacción del usuario. 

 

Capítulo 3: Materiales y Componentes 

 detalla los componentes y materiales que se usan en el sistema de cortina automática. Cada componente hace algo específico en la operación y control de la cortina, y su integración permite la automatización basada en la intensidad de la luz ambiental. 

1. ESP32 

El ESP32 es el microcontrolador central del sistema. Este dispositivo es fundamental para proyectos de automatización ya que su capacidad de procesamiento, bajo consumo de energía y conectividad integrada WiFi y Bluetooth. Estas características permiten no solo el control local de la cortina, sino también la posibilidad de integración con aplicaciones móviles o plataformas de domótica. En este proyecto, el ESP32 recibe señales del sensor de luz y envía comandos al motor para ajustar la posición de la cortina según la intensidad de luz detectada. 

2. Arduino 8600 

El Arduino 8600 se usa como una placa auxiliar en el proyecto. Aunque el ESP32 actúa como el controlador principal, el Arduino 8600 permite gestionar otros aspectos del sistema, como el monitoreo de parámetros adicionales y la conexión de componentes que requieren control de voltaje específico o manejo de señales. La flexibilidad y compatibilidad con otros dispositivos facilitan su uso en sistemas de automatización. 

3. Sensor de Luz (LDR - Resistor Dependiente de la Luz) 

El sensor de luz, específicamente un LDR, es el componente que mide la intensidad de la luz en el ambiente. Basado en el principio de fotoconductividad, su resistencia disminuye a medida que aumenta la cantidad de luz. El ESP32 lee estos cambios en resistencia como variaciones de voltaje, lo que le permite determinar cuándo la cortina debe ajustarse para regular la luz en el interior del espacio. 

4. Motor paso a pasos(Stepper Motor) + Driver ULN2003 

El motor paso a paso es el componente encargado de mover la cortina. A diferencia de otros motores, el motor a pasos permite un control preciso del movimiento y es ideal para aplicaciones que requieren ajustes incrementales, como el control de una cortina. El driver ULN2003 actúa como una interfaz entre el microcontrolador y el motor, gestionando el flujo de corriente necesario para operar el motor de forma segura y eficiente. 

5. Placa de Circuito 

La placa de circuito es el soporte sobre el cual se montan y conectan todos los componentes electrónicos. Esta placa organiza el sistema, permite conexiones seguras y reduce el espacio necesario para los componentes. Al diseñar el circuito sobre una placa, se asegura la estabilidad de las conexiones y se facilita el mantenimiento del sistema. 

6. Pineras y Cables Dupont 

Las pineras y los cables Dupont son esenciales para las conexiones entre los diferentes módulos del sistema. Las pineras proporcionan puntos de contacto seguros para conectar componentes a la placa de circuito, mientras que los cables Dupont permiten la transmisión de señales y corriente eléctrica entre los dispositivos. Estos elementos simplifican el proceso de ensamblaje y mejoran la organización del circuito. 

7. Resistencias 

Las resistencias regulan el flujo de corriente en el sistema, protegiendo componentes sensibles, como el sensor de luz, de variaciones de voltaje. En este proyecto, las resistencias ajustan el nivel de señal de salida del LDR, asegurando que el ESP32 reciba datos precisos sobre la intensidad de la luz. 

8. Borneras 

Las borneras son conectores que permiten realizar conexiones seguras y desmontables entre componentes eléctricos, facilitando el montaje y el mantenimiento del sistema. En este proyecto, las borneras son útiles para conectar y desconectar el motor y otros componentes sin tener que desmontar todo el circuito. 

9. Focos Inteligentes 

Los focos inteligentes se integran al sistema para proporcionar iluminación adicional cuando la luz natural es insuficiente. Estos focos pueden controlarse a través del ESP32 y permiten ajustar la intensidad y el color de la luz de manera remota o automática. Su inclusión en el sistema contribuye al control total de la iluminación en el espacio. 

10. Dimmer 

El dimmer es un dispositivo que permite variar la intensidad de los focos inteligentes. A través del ESP32, el sistema puede ajustar la iluminación artificial según la luz natural disponible. Este componente es clave para la eficiencia energética, ya que permite el control preciso de la luz, reduciendo el consumo cuando hay suficiente luz solar y aumentando la intensidad cuando es necesario. 

 

 

Capítulo 4: Diseño del Sistema 

El capítulo detalla el diseño del sistema de la cortina automática sensible a la luz solar. El sistema está compuesto por diversos componentes que trabajan en conjunto para ajustar la posición de la cortina en función de los niveles de luz ambiental.  

1. Diagrama de Bloques 

El diseño del sistema se presenta en el siguiente diagrama de bloques, donde se observa cómo cada componente interactúa con el sistema de control central: 

    Sensor de Luz (LDR): Detecta los niveles de luz en el ambiente y envía una señal de voltaje variable al microcontrolador. 

    ESP32: Actúa como el núcleo de control del sistema, procesando las señales del sensor de luz y enviando comandos al motor y los focos inteligentes. 

    Motor a Pasos + Driver ULN2003: Ejecuta las órdenes del ESP32 para ajustar la posición de la cortina en respuesta a los cambios en la intensidad de la luz. 

    Focos Inteligentes + Dimmer: Reciben instrucciones del ESP32 para ajustar la intensidad de la luz artificial según los niveles de luz natural. 

    Arduino 8600: Colabora en el control de la iluminación, permitiendo una integración fluida de los focos inteligentes y el dimmer al sistema. 

2. Funcionamiento General 

El sistema de cortina automática opera bajo un esquema de retroalimentación, donde el sensor de luz detecta la intensidad de la luz ambiental y transmite esta información al ESP32, que actúa como unidad de procesamiento central. Según los umbrales de luz programados, el ESP32 decide si debe enviar una señal al motor para abrir o cerrar la cortina, o si debe ajustar la iluminación artificial mediante el dimmer y los focos inteligentes. 

Modo de Operación 

    Luz Alta: Cuando el sensor de luz detecta una alta intensidad de luz solar, el ESP32 activa el motor a pasos para cerrar la cortina y así reducir el ingreso de luz en el espacio. 

    Luz Baja: Si el sensor de luz registra niveles bajos de luz, el ESP32 abre la cortina para permitir el ingreso de luz natural y, si es necesario, ajusta los focos inteligentes para proporcionar iluminación adicional. 

    Integración con Iluminación Artificial: En niveles de luz intermedios, el ESP32 puede activar los focos inteligentes y controlar su intensidad mediante el dimmer, de modo que la luz artificial complemente la luz natural disponible. 

3. Flujo de Datos y Control 

El flujo de control se basa en los datos del sensor de luz. A continuación, se describe el proceso de funcionamiento en detalle: 

    Medición de Luz Ambiental: El sensor de luz (LDR) mide continuamente la intensidad luminosa y envía un valor analógico al ESP32. 

    Procesamiento en el ESP32: El ESP32 convierte el valor analógico en un dato digital, lo compara con los umbrales preestablecidos y determina si la cortina debe abrirse o cerrarse. 

    Control del Motor a Pasos: Si el ESP32 decide que la cortina debe ajustarse, envía una señal al driver ULN2003, el cual controla la corriente que mueve el motor a pasos en la dirección requerida (abrir o cerrar la cortina). 

    Ajuste de Iluminación Artificial: En condiciones de poca luz, el ESP32 envía comandos al Arduino 8600 para controlar el dimmer y ajustar la intensidad de los focos inteligentes según las necesidades del espacio. 

4. Integración de la Iluminación Inteligente 

La iluminación inteligente se integra al sistema para optimizar el uso de la luz artificial en el espacio. Esta integración permite que el sistema ajuste los focos según la disponibilidad de luz natural. Cuando la luz exterior es insuficiente, el ESP32 activa los focos inteligentes y ajusta su intensidad a través del dimmer para mantener una iluminación adecuada en el ambiente. 

5. Diagramas de Circuito 

A continuación se presenta una descripción del diagrama de circuito, que muestra cómo están conectados los componentes principales: 

    Conexión del Sensor de Luz: El sensor de luz se conecta al ESP32 a través de un pin de entrada analógica, de modo que el microcontrolador pueda leer los cambios de voltaje que reflejan los niveles de luz. 

    Control del Motor: El motor a pasos se conecta al ESP32 a través del driver ULN2003, que permite un control de dirección y velocidad precisos. 

    Integración del Dimmer y Focos Inteligentes: Los focos y el dimmer están conectados al Arduino 8600, que recibe instrucciones del ESP32 para ajustar la iluminación artificial según las condiciones ambientales. 

6. Algoritmo de Control 

El funcionamiento del sistema se basa en un algoritmo de control programado en el ESP32, el cual realiza las siguientes funciones: 

    Inicialización: El sistema se enciende y el ESP32 calibra el sensor de luz y establece los umbrales de operación. 

    Lectura Continua del Sensor: El ESP32 lee los valores de luz del sensor cada cierto intervalo de tiempo (por ejemplo, cada segundo). 

    Evaluación de Condiciones: Si el valor de luz supera el umbral alto, el ESP32 activa el motor para cerrar la cortina. Si el valor de luz está por debajo del umbral bajo, el ESP32 activa el motor para abrir la cortina. 

    Control de Iluminación: Si la luz natural es insuficiente, el ESP32 activa los focos inteligentes a través del Arduino 8600 y ajusta su intensidad con el dimmer. 

    Retroalimentación y Ajustes: El sistema monitorea continuamente el entorno y realiza ajustes automáticos en la posición de la cortina y la intensidad de la luz artificial para mantener un ambiente confortable. 

 

 

 
