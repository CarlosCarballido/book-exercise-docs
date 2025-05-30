# Gateway Device Application (Connected Devices)

## Lab Module 07

Be sure to implement all the PIOT-GDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do?

La implementación permite la comunicación bidireccional del GDA a través de MQTT. El cliente MQTT está diseñado para publicar datos y suscribirse a temas, facilitando la recepción de información en tiempo real. Para lograr esto, se desarrolló la clase MqttClientConnector, encargada de establecer la conexión, gestionar la publicación y suscripción de mensajes, así como manejar los eventos asociados al protocolo. Esta clase se integra dentro de DeviceDataManager y se activa conforme a la configuración establecida.

How does your implementation work?

Para gestionar la comunicación MQTT de manera asincrónica, la implementación utiliza la librería Paho. La clase MqttClientConnector se encarga de configurar y administrar la conexión con el broker, permitiendo publicar mensajes, suscribirse a temas y gestionar los eventos propios del protocolo MQTT. Esta clase está integrada dentro de DeviceDataManager y se activa en función de la configuración establecida. Su correcto funcionamiento fue comprobado mediante análisis con Wireshark.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: <https://github.com/CarlosCarballido/java-components/tree/labmodule7>

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

EOF.
