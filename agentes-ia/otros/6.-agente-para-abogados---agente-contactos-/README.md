```markdown
# 6. Agente para Abogados - Agente Contactos

## Descripción  
Workflow diseñado para gestionar y asistir con consultas relacionadas a contactos en el ámbito legal, integrando inteligencia artificial y hojas de cálculo para ofrecer respuestas precisas y actualizadas.

## Requisitos  
- Credenciales para acceso a OpenAI (para el nodo `lmChatOpenAi`)  
- Credenciales de Google Sheets con permisos de lectura y escritura (para el nodo `googleSheetsTool`)  
- Configuración de credenciales dentro de n8n para los nodos:  
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`  
  - `n8n-nodes-base.googleSheetsTool`  
  - `@n8n/n8n-nodes-langchain.agent`

## Instrucciones de configuración  
1. Añadir credenciales de OpenAI en n8n con las claves correspondientes.  
2. Configurar credenciales de Google Sheets con acceso a la hoja de contactos relevante.  
3. Importar el workflow en n8n y verificar que los nodos están vinculados correctamente a sus credenciales.  
4. Revisar y ajustar cualquier parámetro personalizado según las necesidades del despacho o equipo legal.

## Detalles de funcionamiento  
El workflow consta de 10 nodos que integran:  
- Un agente de IA basado en Langchain para procesar consultas y generar respuestas contextuales.  
- Acceso y modificación de datos en Google Sheets para mantener actualizados los contactos.  
- Nodos de configuración y activación para desencadenar el flujo de manera eficiente y controlada.  

Este agente permite la interacción con una base de datos de contactos legales, facilitando el acceso rápido a información clave mediante procesamiento natural del lenguaje.

## Ejemplos de uso  
- Consultar detalles de un contacto específico solicitando su nombre o información relevante.  
- Añadir o actualizar información de contacto en la hoja de cálculo mediante comandos naturales.  
- Recibir respuestas contextuales basadas en el historial y datos almacenados, optimizando la gestión de contactos del equipo legal.

---
Categoría: agentes-ia/otros  
Número de nodos: 10  
Tipos de nodos utilizados:  
- `@n8n/n8n-nodes-langchain.lmChatOpenAi`  
- `n8n-nodes-base.googleSheetsTool`  
- `@n8n/n8n-nodes-langchain.agent`  
- `n8n-nodes-base.set`  
- `n8n-nodes-base.executeWorkflowTrigger`  
```