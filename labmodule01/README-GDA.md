# Gateway Device Application (Connected Devices)

## Lab Module 01

Be sure to implement all the PIOT-GDA-* issues (requirements).

### Description

The Gateway Device Application (GDA) acts as a bridge between constrained IoT devices and cloud-based services. 
It collects, processes, and forwards data from constrained devices, ensuring efficient communication and data management.
This implementation includes setting up communication protocols, handling device interactions, and enabling reliable 
data transmission between sensors, actuators, and cloud platforms.

The GDA is developed in Java and includes modules for device management, data transformation, and connectivity 
with external cloud services. The system ensures proper logging, error handling, and scalability to accommodate 
various IoT scenarios.

### Code Repository and Branch

URL: [https://github.com/CarlosCarballido/java-components](https://github.com/CarlosCarballido/java-components)  
Branch: `default`

### Unit Tests Executed

- ConfigUtilTest
- GatewayDeviceAppTest
- SystemCpuUtilTaskTest
- SystemMemUtilTaskTest
- ResourceNameTest

### Integration Tests Executed

- DeviceDataManagerTest
- CloudClientConnectorTest
- MqttClientConnectorTest
- CoapClientConnectorTest
- SensorDataTest
- DataIntegrationTest

EOF.
