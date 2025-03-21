# Constrained Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Esta implementación realiza modificaciones en el SystemPerformanceManager para que pueda recoger datos de telemetría relacionados con la CPU y la memoria. Además, se introducen cambios en DataUtil para permitir la conversión entre los datos de sensores, actuadores y rendimiento en formato JSON, y viceversa, de JSON a los tipos de datos originales. Este proceso facilita la comunicación adecuada entre los distintos componentes del sistema.

How does your implementation work?

La implementación se puede describir de la siguiente manera:

SystemPerformanceManager se ajusta para capturar la telemetría de la CPU y la memoria, añadiendo un setter para el dataMessageListener.

En cuanto a DataUtil, se modifican sus métodos para que conviertan los datos de sensores, actuadores y rendimiento a JSON, y también para realizar la conversión inversa de JSON a los tipos de datos originales. Esto asegura la correcta interacción entre los componentes del sistema. Los métodos clave son:

def_formatDataAndLoadDictionary: Este método toma una cadena JSON y la transforma en un diccionario, manejando adecuadamente los tipos de datos booleanos y decimales.
def_generateJsonData: Se utiliza para convertir un objeto en una cadena JSON, permitiendo configuraciones para codificación UTF-8 y formato de indentación.
def_updateIotData: Actualiza un objeto con los datos provenientes de un diccionario JSON, asignando los valores correspondientes a sus atributos.
Con estas modificaciones, se asegura que el sistema pueda manejar y procesar los datos de manera efectiva.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: https://github.com/CarlosCarballido/python-components/tree/labmodule05

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest
- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest
- tests de part02/unit/data
- tests de part02/unit/sim

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ConstrainedDeviceAppTest
- SystemPerformanceManagerTest
- DeviceDataManagerNoCommsTest
- DataIntegrationTest
- test de part02/integration/emulated
- test de part02/integration/system

EOF.
