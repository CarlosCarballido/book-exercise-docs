# Gateway Device Application (Connected Devices)

## Lab Module 11

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do?

La implementación facilita la comunicación segura entre el GDA local y el servicio Ubidots en la nube mediante MQTT. Envía información de sensores y rendimiento, recibe eventos relacionados con actuadores y los retransmite al CDA para activar dispositivos como el LED.

How does your implementation work?

Mi implementación funciona mediante la clase CloudClientConnector, que usa MqttClientConnector para conectarse de forma segura al cloud de Ubidots con credenciales y certificados. Gestiona conexiones, suscripciones y mensajes, enviando datos de sensores y rendimiento desde el GDA a la nube. Además, recibe eventos de actuadores desde la nube, los convierte en ActuatorData y los envía al CDA para activar dispositivos como el LED.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: <https://github.com/CarlosCarballido/java-components/tree/labmodule-11>

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
- CloudClientConnectorTest

EOF.
