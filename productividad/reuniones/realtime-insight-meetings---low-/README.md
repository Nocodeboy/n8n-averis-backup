```markdown
# Realtime insight meetings - Low

## Descripción  
Este workflow está diseñado para optimizar la productividad en reuniones, generando insights en tiempo real mediante la integración de OpenAI y bases de datos PostgreSQL/Supabase. Permite automatizar el procesamiento y análisis de datos durante las reuniones para facilitar la toma de decisiones rápidas y precisas.

## Requisitos  
- Cuenta y credenciales de OpenAI para el nodo `@n8n/n8n-nodes-langchain.openAi`  
- Acceso a una base de datos PostgreSQL y/o Supabase (host, usuario, contraseña, base de datos)  
- Instancia de n8n con los nodos mencionados instalados y habilitados  

## Instrucciones de configuración  
1. Configure las credenciales de OpenAI en n8n (API Key).  
2. Configure las credenciales para la base de datos PostgreSQL y Supabase en n8n.  
3. Importe el workflow en su instancia de n8n.  
4. Ajuste los parámetros de conexión y consulta SQL según su base de datos.  
5. Defina las URLs y endpoints si utiliza nodos de Webhook y HTTP Request.  
6. Verifique que los nodos condicionales (If) y de estado (Sticky Note, Set) tengan los valores adecuados para su flujo.  

## Detalles de funcionamiento  
- El workflow inicia con un Webhook que recibe datos relacionados con la reunión.  
- Utiliza nodos HTTP Request para obtener información adicional si es necesario.  
- Consulta datos almacenados en bases PostgreSQL/Supabase para contexto previo.  
- Envía entradas procesadas a OpenAI para generar insights o resúmenes en tiempo real.  
- Controla el flujo condicionalmente con nodos If para manejar diferentes escenarios.  
- Utiliza Sticky Notes para documentar estados clave dentro del flujo.  
- Finalmente, actualiza o inserta información relevante en la base de datos para seguimiento.  

## Ejemplos de uso  
- Automatizar la generación de resúmenes y recomendaciones durante reuniones de equipo.  
- Monitorear indicadores clave en tiempo real y obtener alertas basadas en datos recientes.  
- Enriquecer reuniones con datos históricos y sugerencias basadas en AI para decisiones informadas.  

---

**Nodos utilizados:**  
`@n8n/n8n-nodes-langchain.openAi`, `n8n-nodes-base.supabase`, `n8n-nodes-base.postgresTool`, `n8n-nodes-base.if`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.set`, `n8n-nodes-base.postgres`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.webhook`  

**Número total de nodos:** 19  
**Categoría:** productividad/reuniones  
```