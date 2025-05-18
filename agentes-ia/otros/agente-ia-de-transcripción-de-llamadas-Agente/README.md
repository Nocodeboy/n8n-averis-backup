```markdown
# Agente IA de transcripción de llamadas

## Descripción

Workflow diseñado para transcribir y procesar llamadas de clientes utilizando inteligencia artificial, integrando múltiples herramientas para gestionar, analizar y distribuir la información obtenida durante el proceso de atención y ventas.

## Requisitos

- Credenciales para OpenAI (API key)
- Cuenta y credenciales API de HubSpot
- Cuenta y credenciales API de Asana
- Cuenta y credenciales API de Gmail
- Acceso a n8n con los nodos necesarios instalados:
  - `@n8n/n8n-nodes-langchain.openAi`
  - `n8n-nodes-base.aggregate`
  - `n8n-nodes-base.hubspot`
  - `n8n-nodes-base.html`
  - `n8n-nodes-base.if`
  - `n8n-nodes-base.asana`
  - `n8n-nodes-base.code`
  - `n8n-nodes-base.gmail`
  - `n8n-nodes-base.stickyNote`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.splitOut`
  - `n8n-nodes-base.httpRequest`
  - `n8n-nodes-base.markdown`
  - `n8n-nodes-base.webhook`

## Instrucciones de configuración

1. Importar el workflow en n8n.
2. Configurar las credenciales para OpenAI, HubSpot, Asana y Gmail en la sección de credenciales de n8n.
3. Ajustar los endpoints y parámetros del nodo `httpRequest` según el proveedor de llamadas o sistema telefónico utilizado.
4. Personalizar reglas y condiciones en los nodos `if` y `code` para adaptarse a las necesidades específicas del flujo de trabajo.
5. Verificar las configuraciones de webhook para la recepción de datos en tiempo real.

## Detalles de funcionamiento

- Captura y recepción de grabaciones o transcripciones de llamadas vía webhook o API.
- Procesamiento y limpieza de texto con nodos `html`, `code` y `set`.
- Transcripción avanzada y análisis semántico mediante OpenAI.
- Agregación y estructuración de datos relevantes con `aggregate`.
- Integración con HubSpot y Asana para creación/actualización de registros y tareas.
- Envío de resúmenes y reportes automáticos por correo electrónico usando Gmail.
- Validaciones y rutas condicionales controladas con nodos `if`.
- Gestión visual y notas internas con `stickyNote` y formato markdown.

## Ejemplos de uso

- Transcribir y analizar llamadas de clientes para mejorar procesos de ventas y soporte.
- Automatizar la generación de tareas de seguimiento en Asana basadas en información clave de las llamadas.
- Actualizar automáticamente datos de contacto y oportunidades en HubSpot tras cada llamada.
- Enviar resúmenes diarios o inmediatos al equipo de ventas mediante email.
- Implementar un sistema de onboarding basado en la información extraída de las llamadas entrantes.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** Agente, Customer / Sales, Onboarding  
**Número de nodos:** 43
```