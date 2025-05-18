```markdown
# Agente IA para sitio web

## Descripción
Workflow que utiliza múltiples agentes de inteligencia artificial para interactuar y asistir en plataformas ecommerce. Emplea modelos de lenguaje y memoria contextual para ofrecer respuestas inteligentes y acciones automatizadas en el sitio web.

## Requisitos
- Credenciales de OpenAI configuradas en n8n para el nodo `lmChatOpenAi`.
- Acceso habilitado a nodos de LangChain (`@n8n/n8n-nodes-langchain`).
- API keys y permisos para cualquier herramienta o workflow externo vinculados en nodos `toolWorkflow`.
- n8n versión compatible con nodos LangChain.

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar la credencial OpenAI en el nodo `lmChatOpenAi`.
3. Ajustar parámetros de memoria en `memoryBufferWindow` según contexto deseado.
4. Revisar y conectar correctamente los workflows o herramientas usadas en `toolWorkflow`.
5. Verificar que el nodo `chatTrigger` esté correctamente configurado para recibir inputs desde el sitio web.
6. Etiquetar el workflow bajo la categoría `agentes-ia/ecommerce` para facilitar su gestión.

## Detalles de funcionamiento
- El nodo `chatTrigger` inicia la interacción al detectar mensajes o consultas del usuario en el sitio web.
- `lmChatOpenAi` genera respuestas utilizando un modelo de lenguaje avanzado.
- `memoryBufferWindow` mantiene el contexto de la conversación para una experiencia coherente.
- `agent` orquesta la coordinación entre múltiples agentes y herramientas.
- `toolWorkflow` permite ejecutar acciones específicas o workflows externos según la conversación.
- El flujo cuenta con 7 nodos que trabajan en conjunto para entregar una experiencia IA integrada y dinámica.

## Ejemplos de uso
- Atención automatizada a clientes para resolver dudas sobre productos y pedidos.
- Recomendaciones personalizadas basadas en el historial de compras y preferencias.
- Gestión de procesos como seguimiento de envíos o actualización de inventario mediante workflows integrados.
- Soporte multicanal con capacidad para escalar consultas complejas a agentes humanos.

---
**Categoría:** agentes-ia/ecommerce  
**Etiquetas:** Multiagentes, Ecommerce, Master  
**Nodos utilizados:** `lmChatOpenAi`, `memoryBufferWindow`, `toolWorkflow`, `agent`, `chatTrigger`  
**Número de nodos:** 7
```