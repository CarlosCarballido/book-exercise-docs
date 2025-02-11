# Constrained Device Application (Connected Devices)

## Lab Module 01

Be sure to implement all the PIOT-CDA-* issues (requirements).

### Description

The Constrained Device Application (CDA) is responsible for collecting, processing, and transmitting data from resource-limited IoT devices. 
It typically runs on embedded systems or edge devices that have limited processing power, memory, and network bandwidth.

The implementation focuses on efficient data acquisition, lightweight communication protocols (such as MQTT or CoAP), 
and optimized resource management. The CDA interacts with sensors and actuators to monitor environmental conditions 
and send real-time data to the Gateway Device Application (GDA) or directly to cloud services.

### Code Repository and Branch

URL: [https://github.com/CarlosCarballido/python-components](https://github.com/CarlosCarballido/python-components)  
Branch: `default`

### Unit Tests Executed

- ConfigUtilTest
- DataUtilTest
- SensorManagerTest

### Integration Tests Executed

- SensorSimAdapterManagerTest
- DeviceDataManagerTest
- CloudConnectivityTest

EOF.
