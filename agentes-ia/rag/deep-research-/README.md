```markdown
# Deep Research

## Descripción
Workflow avanzado para llevar a cabo investigaciones profundas utilizando agentes de IA y técnicas de recuperación aumentada de información (RAG). Combina integración con Google Sheets, procesamiento con modelos de lenguaje, gestión de datos y automatización de correo para facilitar investigaciones complejas.

## Requisitos
- Credenciales de Google Sheets con acceso al/los documento(s) correspondiente(s).
- API key de OpenRouter para nodos @n8n/n8n-nodes-langchain.lmChatOpenRouter.
- Configuración de cuenta Gmail para envío y recepción de correos mediante n8n-nodes-base.gmail.
- Acceso a API externas según configuraciones de nodos `httpRequest`.
- n8n versión compatible con nodos de LangChain y la cantidad de nodos requerida.

## Instrucciones de configuración
1. **Google Sheets**: Configure las credenciales en n8n para que el nodo `googleSheets` pueda acceder a las hojas necesarias.
2. **OpenRouter**: Añada su API key en las credenciales de LangChain para el nodo `lmChatOpenRouter`.
3. **Gmail**: Configure las credenciales OAuth2 para el nodo de Gmail.
4. **APIs externas**: Complete las configuraciones y credenciales necesarias para nodos `httpRequest`.
5. Importar el workflow en n8n y ajuste cualquier parámetro personalizado según su contexto.
6. Active el workflow y pruebe con un formulario o disparador apropiado (`formTrigger`).

## Detalles de funcionamiento
- El workflow utiliza 93 nodos combinando fuentes de datos (Google Sheets), procesamiento y agregación (aggregate, switch, limit, merge).
- Integra modelos de lenguaje a través de LangChain para generación y análisis de texto.
- Gestiona lógica condicional y splits para manejar diferentes caminos de datos.
- Automatiza tareas de correo electrónico para notificaciones o seguimiento.
- Incluye nodos de código y HTML para personalizados y visualización interna.
- Soporta parsing estructurado de salida para facilitar interpretaciones posteriores.
- Utiliza nodos tipo stickyNote para documentación interna y organización del workflow.

## Ejemplos de uso
- Realizar una investigación de mercado combinando datos estructurados y análisis de texto automatizado.
- Monitorizar información recolectada vía formularios y generar reportes inteligentes.
- Ejecutar búsquedas y recuperación de información compleja con agentes IA para apoyo en toma de decisiones.
- Enviar resultados o alertas automatizadas por Gmail basadas en análisis procesados.

---

**Categoría:** agentes-ia/rag  
**Número de nodos:** 93  
**Nodos utilizados:** `googleSheets`, `aggregate`, `switch`, `limit`, `merge`, `lmChatOpenRouter`, `html`, `formTrigger`, `code`, `gmail`, `agent`, `set`, `stickyNote`, `outputParserStructured`, `splitOut`, `httpRequest`.
```