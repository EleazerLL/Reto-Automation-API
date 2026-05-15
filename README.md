🚀 Reto de Automatización: API Testing con Karate DSL
Este proyecto contiene la suite de pruebas automatizadas para la validación de servicios REST, enfocándose en la consistencia de datos, manejo de estados HTTP y flujos completos de ciclo de vida de usuario (CRUD).

🛠️ Stack Tecnológico
Para garantizar la compatibilidad del entorno, se han utilizado las siguientes versiones:

Java: JDK 17

Build Tool: Maven 3.8.x

Framework: Karate DSL 1.4.1

Reportes: Cucumber Reports / Karate Reports



🎯 Alcance de las Pruebas
La suite cubre los siguientes escenarios críticos solicitados en la evaluación:

1. Flujo CRUD Completo: Creación, consulta, actualización y eliminación de usuarios en un solo flujo lógico para garantizar la integridad de la data.

2. Data-Driven Testing (Scenario Outline): Uso de tablas de ejemplos (Examples) para validar la creación de múltiples perfiles de usuario con una sola estructura de prueba.

3. Manejo de Datos Dinámicos: Implementación de funciones JavaScript para la generación de correos electrónicos aleatorios, evitando colisiones de datos (Email duplicado).

4. Casos Negativos: Validación de respuestas de error (Status 422 Unprocessable Entity) cuando se envían payloads incompletos.

5. Validación de Esquemas: Verificación de que la estructura JSON de respuesta cumpla con el contrato definido.



⚙️ Configuración y Variables de Entorno

El proyecto utiliza un archivo karate-config.js para centralizar la configuración:

* Base URL: Definida según el ambiente de pruebas.

* Autenticación: Manejo de Bearer Token configurado globalmente para todas las peticiones.



🏃 Ejecución de Pruebas
Para ejecutar los tests desde la terminal, utiliza el siguiente comando de Maven:

Bash
* mvn clean test "-Dkarate.options=--tags @smoke"
(Nota: Puedes omitir los tags para ejecutar la suite completa).



📊 Reportes
Al finalizar la ejecución, los resultados se pueden visualizar en:

* target/karate-reports/karate-summary.html