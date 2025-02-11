# Constrained Device Application (Connected Devices)

## Lab Module 01

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

The Constrained Device Application (CDA) is designed for IoT devices with limited resources. 
It is responsible for collecting sensor data, processing it locally, and sending relevant information to 
the Gateway Device Application (GDA) or cloud services. The CDA ensures efficient resource management and uses 
lightweight communication protocols like MQTT or CoAP for data transmission.

This implementation is developed in Python and focuses on optimizing sensor interactions, handling real-time data 
processing, and providing a reliable connection between edge devices and the broader IoT network.

### Code Repository and Branch

URL: [https://github.com/CarlosCarballido/python-components](https://github.com/CarlosCarballido/python-components)  
Branch: `default`

### Unit Tests Executed

- ConfigUtilTest.py
- SystemCpuUtilTaskTest.py
- SystemMemUtilTaskTest.py
- DataUtilTest.py
- SensorDataTest.py
- BaseIotDataTest.py
- ActuatorDataTest.py

### Integration Tests Executed

- ConstrainedDeviceAppTest.py
- DeviceDataManagerWithCommsTest.py
- DeviceDataManagerIntegrationTest.py
- DeviceDataManagerWithMqttClientOnlyTest.py
- DeviceDataManagerCallbackTest.py
- MqttClientConnectorTest.py
- CoapClientConnectorTest.py
- CoapClientPerformanceTest.py
- CoapServerAdapterTest.py
- SensorAdapterManagerTest.py
- ActuatorAdapterManagerTest.py
- DataIntegrationTest.py
- SensorPerformanceDataTest.py
- TemperatureEmulatorTaskTest.py
- SensorEmulatorManagerTest.py
- HumidityEmulatorTaskTest.py
- PressureEmulatorTaskTest.py
- ActuatorEmulatorManagerTest.py
- ActuatorSimTaskTest.py
- TemperatureSensorSimTaskTest.py
- HumidifierActuatorSimTaskTest.py
- PressureSensorSimTaskTest.py
- HumiditySensorSimTaskTest.py

EOF.
