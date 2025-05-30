# Lab Module 12 - Semester Project - Final Write-up

NOTE: Be sure to implement all the Lab Module 12 requirements listed at Lab Module 12.


## Description

Describe your idea in 1 paragraph (at least 2 or 3 sentences).

Mi proyecto consiste en desarrollar un sistema de monitoreo y control basado en IoT que detecta la presencia de gases invisibles en diferentes entornos mediante sensores simulados. Utilizando protocolos como MQTT y CoAP, el sistema permite la comunicación bidireccional entre dispositivos (CDA y GDA) y la nube, facilitando el envío de datos en tiempo real y la activación automática de actuadores, como ventiladores, para mitigar riesgos. Esta solución busca mejorar la seguridad y la prevención en espacios industriales y domésticos mediante una arquitectura eficiente y escalable.

## What - The Problem 

What problem did you tackle and why does it matter? Write 1 to 2 paragraphs in response.

Este proyecto se centra en mitigar el peligro que representan los gases invisibles, los cuales pueden filtrarse en diferentes ambientes sin ser detectados fácilmente por las personas. La ausencia de detección temprana de estos gases puede provocar situaciones de riesgo significativo para la salud y la seguridad, incluyendo intoxicaciones, explosiones o daños ambientales.

Por ello, es fundamental contar con un sistema capaz de identificar la presencia de estos gases de manera rápida y confiable, permitiendo una respuesta inmediata para minimizar impactos negativos. Esta solución contribuye a proteger tanto a las personas como a las infraestructuras, mejorando la prevención y gestión de riesgos en entornos vulnerables.

## Why - Who Cares? 

Why do you care about this particular problem? Write 1 to 2 paragraphs in response.

Me interesa este problema porque las fugas de gases en entornos industriales o laborales no solo amenazan la seguridad de las personas, sino que también pueden causar daños materiales severos y pérdidas económicas significativas. La detección temprana y la respuesta automática ante estos incidentes son clave para evitar accidentes graves, garantizar un ambiente de trabajo seguro y cumplir con normativas de seguridad cada vez más estrictas.

Además, desarrollar un sistema automatizado que monitorice constantemente y actúe ante la presencia de gases nocivos contribuye a la prevención proactiva, minimizando riesgos antes de que se conviertan en emergencias. Este enfoque tecnológico tiene un impacto directo en la protección de vidas humanas y en la sostenibilidad de las operaciones industriales, razones por las que considero que abordar este problema es crucial.

## How - Expected Technical Approach

Write 1 to 2 paragraphs describing the outcomes you achieved.

Desarrollé un emulador que simula lecturas realistas de un sensor de gas, generando valores variables que reflejan concentraciones cambiantes. Estos datos se transmiten desde el CDA al GDA a través de MQTT, donde se procesan y posteriormente se envían a la nube para su almacenamiento y visualización en dashboards, facilitando así el monitoreo remoto y en tiempo real.

Adicionalmente, implementé la emulación de un ventilador actuador que puede recibir comandos para activarse o desactivarse según los niveles de gas detectados, permitiendo una respuesta automatizada frente a situaciones de riesgo. Este conjunto funcional demuestra la viabilidad de un sistema integral de detección y actuación basado en sensores y actuadores virtuales.

### System Diagram

Embed a block diagram depicting your overall design, including the CDA, GDA, and Cloud Services interactions.
Be sure to include arrows depicting data flow from one application / service to the next.

```plaintext
+----------------+      MQTT      +----------------+      MQTT      +----------------+
|      CDA       | <------------> |      GDA       | <------------> |     Cloud      |
| (Sensor & Act.)|                | (Procesamiento)|                | (Almacenamiento|
|                |                |                |                |   y Visual.)   |
+----------------+                +----------------+                +----------------+
         ↑                               ↓                               
         |←------ Comandos Actuador -----|                                
```

Write 1 to 2 paragraphs describing your design.

Descripción del diseño:

En este esquema, el CDA funciona como generador de datos, simulando lecturas de sensores que se envían al GDA mediante MQTT. El GDA procesa esta información y realiza dos funciones principales: por un lado, envía los datos relevantes a la nube para su almacenamiento y análisis; por otro, genera comandos de control para los actuadores, como el ventilador, que son enviados de vuelta al CDA para activar o desactivar dichos dispositivos según las condiciones detectadas. Esta arquitectura permite un flujo de información eficiente y bidireccional, facilitando tanto el monitoreo remoto como la respuesta automática ante eventos críticos.

### What THREE (3) sensors and ONE (1) actuator did you use (add more if you wish)?

- CDA Sensor 1: Presión

- CDA Sensor 2: Temperatura

- CDA Sensor 3: Humedad

- CDA Actuator 1: Ventilador

### What ONE (1) CDA protocol and TWO (2) GDA protocols did you implement (add more if you wish)?

- CDA to GDA Protocol: MQTT

- GDA to CDA Protocol: MQTT

- GDA to Cloud Protocol: MQTT

- Cloud to GDA Protocol: MQTT

### What TWO (2) cloud services / capabilities did you use (add more if you wish)?

- Cloud Service 1 (data ingress - all inputs):

- Cloud Service 2 (data egress - all actuation events):

## Screen Shots Representing Cloud Services

### Screen Shots Representing Visualized Data

NOTE: Include (at least) TWO (2) screen shots - one showing at least 1 hour
of time-series data from the CDA, and one showing an event being triggered
that results in an actuation event sent to your GDA and then to your CDA.

EOF.
