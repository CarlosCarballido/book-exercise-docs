# Gateway Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-GDA-* issues.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Punto de entrada:
La aplicación GatewayDeviceApp es el componente más general y sirve como punto de entrada del sistema. Su función principal es iniciar el sistema y registrar cada paso, ya sean éxitos o errores. Por el momento, actúa simplemente como un contenedor que envuelve a SystemPerformanceManager.

Núcleo de la implementación:
SystemPerformanceManager constituye el corazón de esta fase. Se encarga de poner en marcha las tareas de monitorización tanto de la CPU como de la memoria secundaria, y de registrar los resultados obtenidos. Esto se realiza mediante dos clases derivadas, SystemCpuUtilTask y SystemMemUtilTask, que implementan los métodos necesarios para capturar las mediciones. Además, este gestor inicia y detiene las tareas de monitorización y mantiene un registro continuo de las mediciones. Desde el inicio, crea un future (basado en un ScheduledExecutorService) que permite ejecutar una tarea de forma asíncrona, consultarla o cancelarla. El ejecutor, configurado para trabajar con un único hilo, ejecuta una tarea Runnable que invoca el método handleTelemetry, el cual a su vez llama a las tareas de monitorización de CPU y memoria secundaria.

Clases específicas de telemetría:
Tanto SystemMemUtilTask como SystemCpuUtilTask heredan de BaseSystemUtilTask. Estas clases encapsulan la funcionalidad descrita en sus nombres: cada una se encarga de obtener y devolver la telemetría correspondiente, ya sea de la CPU o de la memoria secundaria.

How does your implementation work?

    Al ejecutar mvn test -Dtest=GatewayDeviceAppTest, se produce un fallo en PIOT-GDA-02-003. Aunque el código se ejecuta, Maven arroja un extenso error en el stacktrace. Sin embargo, al desactivar los tests en el archivo pom.xml, el código funciona correctamente.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/CarlosCarballido/java-components/tree/labmodule02


### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- 
- 
- 

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- 
- 
- 

EOF.
