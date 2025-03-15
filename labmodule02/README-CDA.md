# Constrained Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the - PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Esta implementación constituye el núcleo del sistema, ya que permite capturar datos de telemetría relacionados con la memoria y el uso de la CPU para su posterior análisis. Aunque en este momento no ejecuta acciones directas, sienta las bases necesarias para monitorizar de manera adecuada la plataforma IoT.

How does your implementation work?

Se define una clase base que centraliza las tareas de adquisición de telemetría, centradas en dos aspectos: la medición de la memoria y el seguimiento del uso de la CPU. Para cada una de estas funciones, existe una clase específica que implementa un método dedicado a obtener las mediciones. La aplicación principal invoca estas clases mediante el método handleTelemetry del gestor de rendimiento, lo que garantiza la monitorización continua del sistema. Además, este gestor es responsable de iniciar y detener las tareas de captura, registrar un historial de las mediciones y configurar parámetros esenciales del sistema, como pollRate y locationID.

- PIOT-CDA-02-000: Se verificó que todos los tests de labmodule01 se ejecutan correctamente.
- PIOT-CDA-02-001: Se conservó el esqueleto sugerido para ConstrainedDeviceApp, pasando todos los tests.
- PIOT-CDA-02-002: Se implementaron el método init y otros componentes en SystemPerformanceManager según las indicaciones, validando el éxito de todos los tests.
- PIOT-CDA-02-003: Se creó una instancia de SystemPerformanceManager vinculada a ConstrainedDeviceApp e integrada en los métodos start, stop y el constructor de la aplicación; los tests confirman que los logs de ambos sistemas se intercalan correctamente en la consola.
- PIOT-CDA-02-004: Se desarrollaron los métodos sugeridos, incorporando decoradores en las propiedades, y se configuró la clase BaseSystemUtilTask para que el método getTelemetryValue sea abstracto, preparando así su implementación futura.
- PIOT-CDA-02-005: Se creó y pasó el test testGetTelemetryValue() junto con la implementación de init.
- PIOT-CDA-02-006: Se volvió a ejecutar y aprobar el test testGetTelemetryValue() tras implementar init.
- PIOT-CDA-02-007: Se ajustó el método init e implementaron handleTelemetry, startManager y stopManager en SystemPerformanceManager, superando la prueba correspondiente.
- PIOT-CDA-02-100: Se validó el correcto funcionamiento de todos los tests de labmodule02 y se realizó el merge con la rama default.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/CarlosCarballido/python-components/tree/labmodule02

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.


- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest
- ConfigUtilTest


### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ConstrainedDeviceAppTest
- SystemPerformanceManagerTest
- 

EOF.
