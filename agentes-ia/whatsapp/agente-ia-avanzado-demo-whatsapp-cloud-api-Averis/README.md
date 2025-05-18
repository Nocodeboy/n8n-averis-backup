```markdown
# Agente IA Avanzado Demo Whatsapp Cloud API

## Descripción

Workflow avanzado que integra un agente de inteligencia artificial con la API de WhatsApp Cloud para gestionar conversaciones inteligentes y automatizadas. Utiliza capacidades de lenguaje natural, herramientas externas, y gestión de memoria para ofrecer respuestas contextuales y precisas.

## Requisitos

- Cuenta y credenciales de WhatsApp Cloud API.
- APIs de OpenAI (modelos GPT, embeddings).
- Acceso a servicios adicionales según nodos usados (Gmail, Redis, Supabase, Evolution API, Google Docs).
- n8n con los nodos instalados:  
  `@n8n/n8n-nodes-langchain`, `n8n-nodes-base`, `n8n-nodes-evolution-api`, `n8n-nodes-evolution-api.evolutionApi` y otros indicados en los nodos utilizados.
- Base de datos PostgreSQL para memoria conversacional (opcional pero recomendado).
- Credenciales para Gmail, Supabase, Redis y otros servicios que el workflow utilice.

## Instrucciones de configuración

1. **WhatsApp Cloud API**: Configurar el webhook para recibir mensajes y gestionar respuestas.
2. **OpenAI**: Ingresar las claves API para los nodos de lenguaje y embeddings.
3. **Bases de datos y memorias**:
   - Configurar conexión a PostgreSQL para memoria Postgres Chat.
   - Configurar Redis para almacenamiento temporal si aplica.
   - Configurar Supabase para vector store.
4. **Servicios externos**:
   - Añadir credenciales de Gmail para enviar notificaciones o emails.
   - Configurar Evolution API, Google Docs y herramientas de cálculo según necesidades.
5. Importar el workflow en n8n y actualizar todas las credenciales vinculadas a los nodos.

## Detalles de funcionamiento

- Utiliza nodos de LangChain para integración con modelos OpenAI y OpenRouter, gestión de memoria y herramientas inteligentes (cálculo, Wikipedia, Google Docs).
- Procesa mensajes entrantes vía webhook de WhatsApp Cloud API.
- Ejecuta lógica avanzada con switches, condicionales e integración con APIs externas.
- Mantiene contexto conversacional almacenado en Redis y PostgreSQL.
- Genera respuestas enriquecidas y estructuradas mediante output parsers.
- Envía notificaciones y maneja tiempos de espera para mejorar la interacción.
- Integra herramientas para cálculo, búsqueda en Wikipedia y consultas a APIs especializadas.

## Ejemplos de uso

- Responder preguntas frecuentes de clientes vía WhatsApp con respuestas generadas por IA.
- Automatizar cálculos complejos y consultas contextualizadas integradas en la conversación.
- Mantener un historial conversacional para soporte personalizado y seguimiento de casos.
- Enviar alertas y correos en función de ciertos disparadores detectados en la conversación.
- Acceder a información en Google Docs o Wikipedia desde la conversación para enriquecer las respuestas.

---

**Categoría:** agentes-ia/whatsapp  
**Etiquetas:** Averis, WhatsApp, Agente  
**Número de nodos:** 92
```