```markdown
# ****** cotizaciones de productos

## Descripción
Workflow diseñado para gestionar y automatizar cotizaciones de productos, integrando fuentes de datos de WooCommerce y aprovechando capacidades avanzadas de procesamiento de lenguaje natural mediante nodos Langchain y OpenAI.

## Requisitos
- Credenciales de WooCommerce con permisos de lectura/escritura.
- API Key de OpenAI para los nodos de lenguaje (lmChatOpenAi, embeddingsOpenAi).
- Acceso a Supabase para el almacenamiento y consulta de vectores en el vectorStoreSupabase.
- Configuración apropiada para nodos Langchain (textSplitter, retrieverVectorStore, chainRetrievalQa).
- n8n instalado con los nodos base y los nodos de Langchain necesarios.

## Instrucciones de configuración
1. Configure las credenciales de WooCommerce en n8n.
2. Introduzca la API Key de OpenAI en las credenciales de n8n.
3. Configure las credenciales y parámetros de Supabase para el vectorStoreSupabase.
4. Ajuste los parámetros de los nodos de Langchain según las necesidades del proyecto.
5. Importe y active el workflow en n8n.
6. Realice pruebas manuales con el nodo manualTrigger para validar el flujo.

## Detalles de funcionamiento
- El workflow comienza con un disparador manual o ejecución de otro workflow.
- Se extraen datos de productos y cotizaciones desde WooCommerce.
- Archivos relacionados se convierten y procesan para su análisis.
- Se utilizan nodos de texto para dividir, transformar y generar embeddings de la información relevante.
- La base de datos vectorial de Supabase permite realizar consultas eficientes mediante técnicas de recuperación vectorial.
- Se generan respuestas y resúmenes automáticos basados en consultas, con soporte de modelos de lenguaje OpenAI.
- Operaciones de agregación se utilizan para consolidar datos antes de la presentación o almacenaje final.

## Ejemplos de uso
- Obtener cotizaciones actualizadas para un conjunto de productos específicos.
- Automatizar la generación de propuestas basadas en datos históricos y análisis semántico.
- Consultar información contextual sobre productos usando lenguaje natural.
- Resumir grandes volúmenes de documentos y datos relacionados con cotizaciones para toma de decisiones rápida.

---

**Número de nodos:** 18  
**Categoría:** ventas/cotizaciones  
**Tipos de nodos utilizados:**  
- n8n-nodes-base.aggregate  
- @n8n/n8n-nodes-langchain.lmChatOpenAi  
- @n8n/n8n-nodes-langchain.embeddingsOpenAi  
- n8n-nodes-base.wooCommerce  
- n8n-nodes-base.manualTrigger  
- n8n-nodes-base.convertToFile  
- n8n-nodes-base.extractFromFile  
- @n8n/n8n-nodes-langchain.vectorStoreSupabase  
- @n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter  
- n8n-nodes-base.set  
- n8n-nodes-base.executeWorkflowTrigger  
- @n8n/n8n-nodes-langchain.retrieverVectorStore  
- n8n-nodes-base.summarize  
- @n8n/n8n-nodes-langchain.documentDefaultDataLoader  
- @n8n/n8n-nodes-langchain.chainRetrievalQa
```