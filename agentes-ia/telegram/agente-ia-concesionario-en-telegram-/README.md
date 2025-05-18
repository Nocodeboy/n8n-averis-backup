```markdown
# Agente IA Concesionario en Telegram

## Descripción
Workflow para n8n que actúa como un agente de inteligencia artificial integrado en Telegram, facilitando la interacción con clientes de un concesionario. Utiliza procesamiento de lenguaje natural, gestión de memoria en Postgres y herramientas como Google Sheets y Google Calendar para ofrecer respuestas inteligentes y gestionar información en tiempo real.

## Requisitos
- Cuenta y credenciales de Telegram Bot API.
- API Key de OpenAI para los nodos de Langchain.
- Acceso a Google Sheets con las hojas de cálculo configuradas.
- Acceso a Google Calendar para herramientas de gestión de agenda.
- Base de datos Postgres para el manejo de memoria del agente.
- Permisos y credenciales necesarios para ejecutar nodos de n8n relacionados.

## Configuración
1. **Telegram**: Configura un bot en Telegram y añade las credenciales en n8n en el nodo `telegramTrigger` y `telegram`.
2. **OpenAI**: Obtén tu API Key de OpenAI y configúrala en los nodos `lmChatOpenAi` y `openAi`.
3. **Google Sheets**: Vincula tu cuenta de Google y asigna la hoja de cálculo destinada para la gestión de datos.
4. **Google Calendar**: Vincula tu cuenta para permitir interacción con el calendario del concesionario.
5. **Postgres**: Configura la base de datos para almacenamiento y recuperación de memoria en el nodo `memoryPostgresChat`.
6. Ajusta parámetros en nodos `switch`, `if` y `code` según las reglas y lógica deseadas para el agente.

## Funcionamiento
- El bot escucha mensajes entrantes desde Telegram.
- Procesa las consultas usando modelos de lenguaje OpenAI.
- Según las condiciones, utiliza Google Sheets para consultas o actualizaciones, y Google Calendar para gestión de citas.
- Gestiona contexto y memoria conversacional en Postgres para mantener la coherencia en diálogos extensos.
- Toma decisiones lógicas mediante nodos `switch` e `if`.
- Ejecuta código personalizado para transformaciones o validaciones específicas.
- Finalmente, responde al usuario directamente en Telegram a través del nodo correspondiente.

## Ejemplos de Uso
- Un cliente envía un mensaje preguntando por disponibilidad de vehículos; la IA responde con datos de Google Sheets.
- Solicitud de agendar una prueba de manejo, que se registra en Google Calendar.
- Recuperación del historial de conversaciones anteriores mediante memoria almacenada en Postgres.
- Respuestas dinámicas adaptadas al contexto y preferencias detectadas en la conversación.

---

**Número de nodos:** 24  
**Categoría:** agentes-ia/telegram  
**Tipos de nodos:** googleSheets, lmChatOpenAi, switch, openAi, telegramTrigger, googleSheetsTool, if, memoryPostgresChat, code, toolWorkflow, telegram, agent, postgres, googleCalendarTool  
```