# 📸 Evidencias de Ejecución y Pruebas — Examen TutorBot

En este directorio se almacenan las capturas de pantalla que acreditan la implementación y validación del nuevo flujo de alerta:

## 📁 Archivos de Evidencia

1. **`canvas_alerta_atascadas.png`**
   - **Descripción**: Captura de pantalla completa del canvas en n8n mostrando el nuevo workflow `TutorBot - Alerta Tutorias Atascadas`.
   - **Elementos a validar**:
     - Nodo `Cada 30 Minutos` (Schedule Trigger).
     - Nodos de lectura de Google Sheets (`Leer Tutorias`, `Leer Estudiantes`, `Leer Tutores`, `Leer Materias`).
     - Nodo `Filtrar Atascadas` (Code JavaScript con la regla $> 45\text{ min}$).
     - Nodo `Hay Atascadas?` (Filter protector).
     - Nodos de salida: `Enviar Alerta Coordinacion (Gmail)` y `Notificar Telegram Coordinacion`.

2. **`prueba_telegram_alerta.png`**
   - **Descripción**: Captura de pantalla del mensaje recibido en Telegram por la coordinación:
     - `🚨 ATENCIÓN: Las siguientes tutorías llevan más de 45 min sin confirmar: [SOL001, SOL002]. Favor verificar con el tutor/estudiante.`

3. **`prueba_correo_coordinacion.png`**
   - **Descripción**: Captura de pantalla del correo HTML recibido en la bandeja de entrada de `julioveg567@gmail.com` con la tabla detallada de tutorías retrasadas.
