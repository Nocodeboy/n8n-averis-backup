# Enriquecimiento de datos de empresas a partir del contenido del sitio web

## Descripción
Workflow diseñado para extraer y enriquecer información de empresas utilizando el contenido de sus sitios web. Combina scraping, procesamiento con OpenAI y actualización de datos en Google Sheets para facilitar investigaciones y procesos de onboarding.

## Requisitos
- Credenciales para Google Sheets con acceso a la hoja de destino.
- API Key de OpenAI para procesamiento y análisis de texto.
- Acceso a internet para realizar solicitudes HTTP y scraping.
- n8n instalado y configurado con los nodos requeridos.

## Instrucciones de configuración
1. Configurar las credenciales de Google Sheets en n8n.
2. Añadir la API Key de OpenAI en las credenciales correspondientes.
3. Definir la hoja de cálculo y el rango de datos de entrada y salida en el nodo Google Sheets.
4. Ajustar los parámetros del nodo HTTP Request para acceder a los sitios web objetivos.
5. Personalizar el código en el nodo Code si se requiere procesamiento específico.
6. Guardar y activar el workflow.

## Detalles de funcionamiento
- **Manual Trigger** inicia el proceso.
- Se obtienen URLs de sitios web desde Google Sheets.
- El nodo **HTTP Request** descarga el contenido HTML de cada sitio.
- **HTML Extract** extrae datos relevantes del contenido.
- Datos extraídos se procesan con OpenAI para generar enriquecimiento adicional.
- El flujo utiliza **SplitInBatches** para manejar múltiples empresas eficientemente.
- Resultados se combinan con los datos originales usando el nodo **Merge**.
- Información enriquecida se escribe de vuelta en Google Sheets.
- Delays son manejados con el nodo **Wait** para evitar sobrecarga y respetar límites de API.

## Ejemplos de uso
- Complementar bases de datos internas con información actualizada de empresas.
- Automatizar la recopilación de datos para procesos de onboarding de clientes.
- Realizar análisis cualitativo de contenido web para investigaciones de mercado.

---

**Categoría:** utilidades/scraping  
**Etiquetas:** Investigación, Onboarding  
**Nodos utilizados:** 11 (Google Sheets, Merge, Manual Trigger, Code, OpenAI, SplitInBatches, HTTP Request, Wait, HTML Extract)