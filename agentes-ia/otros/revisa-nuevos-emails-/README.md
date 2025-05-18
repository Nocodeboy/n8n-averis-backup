```markdown
# Revisa nuevos Emails

## Descripción
Workflow diseñado para revisar, analizar y gestionar nuevos correos electrónicos mediante agentes IA y nodos integrados de n8n. Automatiza la lectura, filtrado y respuesta o acciones adicionales sobre emails entrantes.

## Requisitos
- Credenciales de Gmail configuradas en n8n para acceso IMAP/SMTP.
- API Key de OpenAI para nodos Langchain (`lmChatOpenAi`, `chainLlm`, `agent`).
- Configuración de Bot de Telegram para notificaciones (opcional).
- Permisos para ejecución de workflows y acceso a nodos de terceros.

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales de Gmail con acceso al buzón deseado.
3. Añade tu API Key de OpenAI en las credenciales de Langchain.
4. Configura el bot de Telegram con token y chat ID para notificaciones si lo utilizas.
5. Ajusta los filtros y condiciones en nodos `switch`, `if` o `filter` para personalizar la revisión.
6. Programa la ejecución periódica en el nodo `scheduleTrigger` según tus necesidades.

## Detalles de funcionamiento
- El workflow se activa según la programación definida en `scheduleTrigger`.
- Recupera correos nuevos mediante el nodo `gmail`.
- Procesa el contenido con nodos Langchain para análisis y toma de decisiones automatizadas.
- Filtra y direcciona emails según criterios definidos en nodos `switch`, `if` y `filter`.
- Ejecuta acciones condicionales, incluyendo respuestas automáticas, disparo de otros workflows o notificaciones por Telegram.
- Utiliza nodos de manipulación como `set`, `code`, `merge` y `splitInBatches` para estructurar y optimizar el flujo.
- Mantiene control y trazabilidad con nodos `stickyNote` y `noOp` para depuración y organización.

## Ejemplos de uso
- Detectar correos importantes y enviar alertas inmediatas por Telegram.
- Responder automáticamente a ciertos tipos de consultas usando LM de OpenAI.
- Integrar con otros workflows para procesar adjuntos o actualizar bases de datos.
- Clasificar emails según contenido y derivar tareas a equipos específicos.

---

**Categoría:** agentes-ia/otros  
**Nodos usados (43):**  
`lmChatOpenAi`, `switch`, `noOp`, `merge`, `chainLlm`, `if`, `filter`, `code`, `executeWorkflow`, `telegram`, `gmail`, `scheduleTrigger`, `set`, `agent`, `stickyNote`, `outputParserStructured`, `splitInBatches`, `httpRequest`
```