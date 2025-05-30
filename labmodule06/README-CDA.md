# Constrained Device Application (Connected Devices)

## Lab Module 06

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Se incorpora soporte para MQTT, habilitando la comunicación entre dispositivos IoT a través del mecanismo de publicación y suscripción a tópicos. Esto permite un intercambio de información en tiempo real entre los distintos elementos del sistema.

How does your implementation work?

La implementación consiste en la configuración de un cliente MQTT que se conecta automáticamente a un broker. Este cliente posibilita la publicación y suscripción a tópicos específicos, facilitando así la transmisión y recepción de datos entre dispositivos. Se incorporaron funciones callback para manejar los mensajes entrantes y gestionar eventos como reconexiones o errores. Gracias a esta estructura, los dispositivos pueden intercambiar información en tiempo real de manera eficiente. Además, se llevaron a cabo pruebas para verificar la compatibilidad y asegurar el correcto desempeño con los demás componentes del sistema.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: <https://github.com/CarlosCarballido/python-components/tree/labmodule06>

### Unit Tests Executed

NOTE: The instructor will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

- unidad 1 y 2

### Integration Tests Executed

NOTE: The instructor will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- Unidad 1 y 2
- MqttClientConnectorTest
- MqttClientControlPacketTest

EOF.
