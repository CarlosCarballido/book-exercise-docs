# Constrained Device Application (Connected Devices)

## Lab Module 03

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

La solución desarrollada se encarga de simular tanto sensores como actuadores en la aplicación ConstrainedDeviceApp, definiendo plantillas específicas para cada tipo de dato. Se establece un conjunto de datos base para un dispositivo IoT, a partir del cual se derivan los datos propios de los sensores y actuadores, incluyendo información como nombre, identificador y valor, entre otros. Se crean sensores para medir humedad, presión y temperatura, y actuadores que simulan el funcionamiento de un humidificador y de un sistema HVAC (calefacción, ventilación y aire acondicionado). Mientras los sensores generan datos de telemetría (por ejemplo, registros de temperatura y humedad), los actuadores se activan o desactivan de forma simulada según su estado. Además, se han desarrollado clases específicas para integrar y gestionar estos elementos, como SensorAdapterManager, ActuatorAdapterManager y DeviceDataManager.

How does your implementation work?

Inicialmente, se define la clase BaseIotData, que sirve como cimiento para ActuatorData, SensorData y SystemPerformanceData. En esta clase se incluyen los atributos básicos comunes (tipo, identificador, estado, nombre, valor, etc.) junto con sus métodos getter y setter. Las clases que la extienden aportan datos particulares para actuadores y sensores, así como métodos adicionales (como el método mágico str).

Seguidamente, se implementa la simulación de sensores comenzando con la clase base BaseSensorSimTask, que recoge la información fundamental y los métodos para generar telemetría, es decir, los metadatos asociados a un sensor genérico. A partir de ella se derivan los sensores de temperatura, presión y humedad; estos heredan los atributos definidos en la clase base y, en versiones futuras, se espera que produzcan información propia mediante el parámetro dataSet del constructor.

De manera similar, se desarrolla la clase BaseActuatorSimTask para simular actuadores. En este caso, los actuadores utilizan un tipo específico de BaseIotData, denominado ActuatorData, que almacena tanto sus estados como las últimas respuestas recibidas. Al recibir un comando, estos dispositivos se activan o desactivan de forma simulada (gestionado mediante datos y logs). Las clases derivadas, como HVAC y Humidifier, implementan básicamente el constructor de la clase padre.

Luego se introduce la clase SensorAdapterManager, cuyo objetivo es centralizar la administración de todos los sensores del sistema. Su constructor configura parámetros esenciales como la frecuencia de actualización, la emulación de datos y la selección de sensores, entre otros. Asimismo, ofrece métodos para iniciar y detener los sensores, y para gestionar la telemetría que estos generan.

El ActuatorAdapterManager sigue principios similares, aunque en lugar de manejar telemetría, se ocupa de administrar los comandos dirigidos a los actuadores y de gestionar sus actualizaciones, lo que permite simular sus activaciones y desactivaciones.

De forma complementaria, la clase DeviceDataManager integra la funcionalidad de ambos gestores y añade el monitoreo del rendimiento del sistema a través de SystemPerformanceManager. Esta clase se encarga de iniciar y detener tanto el SystemPerformanceManager como el SensorAdapterManager, y de gestionar la comunicación con el ActuatorAdapterManager mediante la recepción de mensajes y el envío de respuestas. Su constructor configura todos los elementos necesarios durante el proceso de inicialización.

Finalmente, se completa la integración creando una instancia de DeviceDataManager dentro de ConstrainedDeviceApp, que actúa como punto de entrada de la aplicación. Esta instancia coordina la acción de los gestores, que a su vez controlan los sensores, actuadores y sistemas de monitoreo, utilizando otras clases auxiliares y plantillas de tipos de datos como se explicó al inicio. Para esta implementación se siguió el código de ejemplo, centrándose en comprender su funcionamiento más que en modificarlo. Por ello, se han implementado métodos start y stop que invocan al DeviceDataManager, eliminando referencias redundantes a SystemPerformanceManager, ya que este se gestiona desde otro módulo. Finalmente, un bucle (potencialmente infinito) se encarga de ejecutar todo desde el método main, y se realizó el merge de la rama dado que todas las pruebas unitarias y de integración se completaron con éxito.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: <https://github.com/CarlosCarballido/python-components/tree/labmodule03>

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ActuatorDataTest
- SensorDataTest
- SystemPerformanceDataTest
- HumiditySensorSimTaskTest
- PressureSensorSimTaskTest
- TemperatureSensorSimTaskTest
- HumidifierActuatorSimTaskTest
- HvacActuatorSimTaskTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- SensorAdapterManagerTest
- ActuatorAdapterManagerTest
- DeviceDataManagerNoCommsTest
- ConstrainedDeviceAppTest
- SystemPerformanceManagerTest

EOF.
