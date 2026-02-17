Flujo de trabajo n8n: Segmentación automatizada de clientes potenciales

Este flujo de trabajo implementa una automatización basada en eventos que se activa mediante Hojas de cálculo de Google (Nueva fila añadida).
Al insertar un nuevo cliente potencial, los datos se normalizan mediante nodos de conjunto (conversión de correo electrónico en minúsculas, recorte y mapeo JSON estructurado).
Un nodo de solicitud HTTP externo utiliza una API pública sin autenticación para enriquecer el conjunto de datos.
Un nodo de conmutación aplica lógica condicional basada en reglas para evaluar los criterios de segmentación.
Según la condición evaluada, el flujo se ramifica en Segmento A, B o C.
Cada rama activa una notificación de Telegram mediante credenciales de token de bot y expresiones de mensaje dinámicas.
Los datos procesados ​​se almacenan persistentemente en Hojas de cálculo de Google mediante operaciones de actualización de fila.
Los registros de ejecución garantizan la trazabilidad y la capacidad de depuración.
Las credenciales se gestionan de forma segura dentro del almacén de credenciales de n8n (sin secretos codificados).
El flujo de trabajo sigue un diseño modular, actualizaciones idempotentes y principios de gestión de datos estructurados.
