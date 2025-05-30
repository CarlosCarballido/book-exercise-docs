# Gateway Device Application (Connected Devices)

## Lab Module 10

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do?

La implementación habilita al GDA para recibir y procesar de manera segura y asíncrona los datos enviados por el CDA a través de MQTT con autenticación y TLS. Se encarga de gestionar automáticamente las suscripciones a los temas del CDA y analiza los datos de humedad recibidos para emitir comandos de actuador cuando se requiera. Adicionalmente, registra y transmite la información de los sensores para su posterior procesamiento.

How does your implementation work?

La implementación emplea MqttAsyncClient para establecer una comunicación asíncrona y segura mediante TLS y autenticación. La clase MqttClientConnector administra la conexión y las suscripciones, utilizando listeners que reciben y validan los mensajes, los cuales son enviados a DeviceDataManager. Este componente analiza los datos recibidos, como la humedad, y genera comandos de actuador cuando detecta valores fuera de los parámetros establecidos.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: <https://github.com/CarlosCarballido/java-components/tree/labmodule-10>

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- ConfigUtilTest
- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest
- ActuatorDataTest
- SensorDataTest
- SystemPerformanceDataTest
- SystemStateDataTest
- DataUtilTest

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- GatewayDeviceAppTest
- SystemPerformanceManagerTest
- DataIntegrationTest
- DeviceDataManagerNoCommsTest
- MqttClientConnectorTest
- MqttClientControlPacketTest
- UpdateResourceHandlerTest
- GetActuatorCommandResourceHandlerTest
- CoapServerGatewayTest
- DeviceDataManagerSimpleCdaActuationTest

EOF.
