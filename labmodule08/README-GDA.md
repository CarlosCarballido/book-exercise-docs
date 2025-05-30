# Gateway Device Application (Connected Devices)

## Lab Module 08

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do?

La implementación facilita la comunicación entre dispositivos mediante el protocolo CoAP. Se creó un servidor CoAP, denominado CoapServerGateway, encargado de registrar dispositivos y gestionar la información a través de handlers especializados para el rendimiento del sistema y los sensores. Además, se incorporó soporte para el manejo de datos de actuadores y la adición dinámica de recursos.

How does your implementation work?

La implementación se basa en la clase CoapServerGateway, la cual inicializa un servidor CoAP y estructura los recursos en rutas jerárquicas. Durante su arranque, registra manejadores específicos que procesan los mensajes POST, PUT y GET de acuerdo con el tipo de datos, tales como sensores, rendimiento y actuadores. Esta clase se integra con DeviceDataManager, permitiendo activar o desactivar el servidor según la configuración establecida, además de ofrecer la posibilidad de añadir recursos de forma dinámica para incrementar la flexibilidad del sistema.

How does your implementation work?

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: <https://github.com/CarlosCarballido/java-components/tree/labmodule-8>

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

EOF.
