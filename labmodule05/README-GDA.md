# Gateway Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Esta implementación desarrolla la funcionalidad de generación y estructuración de datos en el dispositivo gateway. La aplicación principal ejecuta un gestor de datos de dispositivos, el cual se encarga de invocar el módulo encargado de gestionar y generar la telemetría relacionada con la memoria, el uso del disco y el procesador del sistema. Para ello, se hace uso de módulos específicos, cada uno de los cuales lleva a cabo una de estas tareas. El objetivo principal es establecer una base sólida para la generación de datos sobre el estado del dispositivo gateway, y así prepararlo para la gestión y transformación de los datos provenientes de los dispositivos conectados.

How does your implementation work?

La implementación se describe a través de los siguientes pasos:

Módulos principales: Se crean los módulos SensorData, ActuatorData, SystemPerformanceData y SystemStateData, que actúan como contenedores de información para los sensores y actuadores. Todos ellos derivan de BaseIoTData, que se implementó previamente. En cada uno de estos módulos, se crean métodos getters y setters para los datos, además de un método handleUpdateData que realiza las operaciones necesarias en el constructor cuando es invocado. Los constructores de estos módulos son específicos para cada uno. Se añadió un módulo opcional, SystemStateData, que recopila una lista de datos tanto de sensores como de actuadores.

Actualización de SystemPerformanceManager: Se modifica SystemPerformanceManager para que pueda manejar los datos de SystemPerformanceData. El método handleTelemetry se ajusta para almacenar los datos de procesador y memoria. Además, se implementa el método generateTelemetry, que genera los datos de SystemPerformanceData y los envía a la nube. También se agrega un IDataMessageListener al constructor para gestionar el paso de mensajes, junto con su correspondiente setter.

Modificaciones en DataUtil: En DataUtil se añaden métodos para convertir los datos de las clases SensorData, ActuatorData, SystemPerformanceData a JSON y viceversa. Se completa la implementación parcial previamente proporcionada y se añade la necesaria para el módulo opcional SystemStateData. Tras ejecutar los tests junto con el CDA, todo se ejecuta correctamente.

Cambios en DeviceDataManager: Se implementan varios cambios en el módulo DeviceDataManager. Su constructor utiliza constantes proporcionadas por un objeto ConfigUtil para configurar la comunicación, y llama a un método privado, initManager, que realiza la inicialización del módulo (por ahora, solo inicializa SystemPerformanceManager). Los métodos startManager y stopManager simplemente llaman a los métodos de inicialización y detención de SystemPerformanceManager. Además, se implementan los métodos de la interfaz IDataMessageListener, junto con varios métodos privados que, por ahora, solo registran logs y verifican datos nulos.

Implementación en GatewayDeviceApp: En el módulo GatewayDeviceApp se utiliza la implementación proporcionada por defecto en la tarea. Básicamente, esto consiste en un envoltorio que proporciona el método main para ejecutar la aplicación en un bucle. GatewayDeviceApp contiene una instancia privada de DeviceDataManager, que se inicia y detiene con los métodos start y stop de sus constructores. La implementación actual es básica, pero funcional.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/CarlosCarballido/java-components/tree/labmodule05


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest
- ResourceNameTest
- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest
- ActuatorDataTest
- SensorDataTest
- BaseIotDataTest
- DataUtilTest
- SystemPerformanceDataTest
- SystemStateDataTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- SystemPerformanceManagerTest
- GatewayDeviceAppTest
- DeviceDataManagerTest
- DataIntegrationTest

EOF.
