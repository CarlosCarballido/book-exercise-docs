# Constrained Device Application (Connected Devices)

## Lab Module 04

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Esta implementación tiene como objetivo vincular los módulos previos con el simulador de la Raspberry Pi, permitiendo simular los sensores y actuadores de la misma. Los datos del emulador se utilizan para generar lecturas de temperatura, humedad y presión, que se muestran en la matriz de LEDs. Además, se establecen conexiones con los actuadores, lo que posibilita el control de la humedad y la temperatura.

How does your implementation work?

Se crean los emuladores de temperatura, humedad y presión, los cuales heredan de la clase BaseSensorSimTask. Se modifica el método generateTelemetry para que devuelvan los valores simulados correspondientes. De manera similar, se crean los emuladores de actuadores (hvac, humidificador, pantalla LED), que también heredan de BaseActuatorSimTask, y se sobrescribe el método generateTelemetry para simular los valores de salida.

Las funcionalidades de los sensores se agrupan en la clase SensorAdapterManager, la cual gestiona los sensores y genera los datos correspondientes. La inicialización de las tareas de sensores se adapta para permitir la integración de los sensores simulados, además de los reales.

Por otro lado, las funcionalidades de los actuadores se reúnen en la clase ActuatorAdapterManager, que gestiona los actuadores, los invoca y genera sus respectivos datos. La inicialización de las tareas de actuadores también se ajusta para incorporar tanto los actuadores simulados como los reales.

Las partes opcionales que requieren la Raspberry Pi no se han implementado debido a la falta de acceso a una Raspberry Pi para realizar las pruebas correspondientes.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: <https://github.com/CarlosCarballido/python-components/tree/labmodule04>

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- all test from part01
- all test from part02

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- SenseHatEmulatorQuickTest
- HumidityEmulatorTaskTest
- PressureEmulatorTaskTest
- TemperatureEmulatorTaskTest
- HumidifierEmulatorTaskTest
- LedDisplayEmulatorTaskTest
- HvacEmulatorTaskTest
- SensorEmulatorManagerTest
- ActuatorEmulatorManagerTest

EOF.
