# Constrained Device Application (Connected Devices)

## Lab Module 12 - Semester Project - CDA Components

Be sure to implement all the PIOT-CDA-* issues (requirements) listed.

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do?

La implementación incorpora soporte para un sensor de gases y un ventilador actuador en el CDA, generando datos simulados que se transmiten mediante MQTT. Además, cuenta con un sensor de luz virtual cuyo ventilador se controla activándose o desactivándose en función de los comandos recibidos desde el GDA.

How does your implementation work?

La implementación consiste en crear tareas emuladoras para el sensor de gas, el ventilador y el sensor de luz. Estos simuladores generan datos y transmiten la información al GDA a través de MQTT o CoAP, siguiendo la misma lógica e integración que los demás dispositivos emulados.

### Code Repository and Branch

NOTE: Be sure to include the branch.

URL: <https://github.com/CarlosCarballido/python-components/tree/labmodule-12>

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
