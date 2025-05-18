```markdown
# Control de Acceso a las Herramientas del Agente según sus roles

## Descripción
Workflow diseñado para gestionar y controlar el acceso a diversas herramientas utilizadas por agentes IA, basándose en sus roles asignados. Permite garantizar que cada agente acceda únicamente a las funcionalidades autorizadas, optimizando la seguridad y personalización del entorno de trabajo.

## Requisitos
- Credenciales válidas para:
  - OpenAI (para nodos `lmChatOpenAi`)
  - Telegram Bot API (para nodos `telegramTrigger` y `telegram`)
  - Airtable API (para almacenar y gestionar información de roles y accesos)
- Acceso configurado a servicios externos según herramientas integradas (Wikipedia, HTTP requests, etc.)
- n8n instalado y con las extensiones correspondientes a los nodos listados.

## Instrucciones de configuración
1. Configure las credenciales de OpenAI, Telegram y Airtable en n8n.
2. Importe el workflow en n8n.
3. Configure las tablas de Airtable con los datos adecuados de agentes y roles.
4. Ajuste los parámetros de los nodos `telegramTrigger` para recibir mensajes y comandos.
5. Revise las reglas de acceso implementadas en los nodos `if` para adecuarlas a su esquema de roles.

## Detalles de funcionamiento
- El workflow inicia con la activación de un trigger en Telegram para recibir solicitudes de agentes.
- Se consulta la base de datos (Airtable) para verificar el rol del agente solicitante.
- Según el rol, se habilitan o restringen diferentes herramientas constituidas por nodos LangChain (calculadora, código, Wikipedia, HTTP Request, etc.).
- La memoria del agente se administra mediante el nodo `memoryBufferWindow` para mantener contexto en las interacciones.
- Condicionales (`if`) controlan el flujo para asegurar la correcta asignación y restricciones.
- Se emplean nodos especializados para ejecutar y orquestar herramientas y código, garantizando un acceso dinámico y seguro.
- Sticky notes se utilizan para documentación interna y seguimiento visual dentro del workflow.

## Ejemplos de uso
- Un agente con rol "Analista" puede acceder a herramientas de cálculo y consultas HTTP para análisis de datos.
- Un agente con rol "Programador" tiene acceso a nodos de ejecución de código y workflows adicionales.
- Agentes sin rol asignado reciben respuestas de acceso denegado y orientación para solicitar permisos.

---

**Categoría:** agentes-ia/otros  
**Número de nodos:** 37  
**Etiquetas:** Base
```