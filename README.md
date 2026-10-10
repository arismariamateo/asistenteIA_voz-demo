# 🩺 MedVoice AI — Recepcionista Virtual Autónoma para Consultorios Médicos

Solución integral de asistencia por voz con Inteligencia Artificial diseñada para consultorios independientes y clínicas odontológicas. Automatiza la atención de pacientes 24/7, responde dudas frecuentes, califica urgencias y gestiona el agendamiento y reprogramación de citas en tiempo real.

---

## 🚀 Demo en Vivo
Puedes probar la experiencia de voz interactiva directamente en la web:
👉 **[Ver Demo en GitHub Pages](https://arismariamateo.github.io/asistenteIA_voz-demo/)**

---

## 🛠️ Arquitectura y Tecnologías

El sistema opera bajo un flujo desacoplado y en tiempo real:

1. **Frontend Web:** 
   - HTML5 semántico con estilos utilitarios mediante **Tailwind CSS**.
   - Integración nativa con **Vapi Web SDK** para comunicación bidireccional de baja latencia vía WebRTC.

2. **Capa de Voz y LLM (Vapi):**
   - Transcripción y síntesis de voz en español con latencia optimizada.
   - Orquestación de funciones (*Function Calling / Tools*) con manejo de fecha y hora local universal.

3. **Backend de Automatización (Make / Ingestion Webhook):**
   - Recepción y parseo de cargas JSON estructuradas.
   - Enrutamiento dinámico según intención:
     - 🚨 **Urgencias:** Notificación inmediata por correo electrónico y registro prioritario.
     - 📅 **Agendamiento / Reagendamiento:** Verificación de slots libres y confirmación.
     - ❌ **Cancelaciones:** Liberación de horarios y actualización de estado.

4. **Persistencia e Integraciones:**
   - **Google Calendar:** Creación, validación y sincronización de eventos de consulta.
   - **Google Sheets:** Base de datos ligera para trazabilidad de llamadas y métricas de conversión.

---

## 📋 Características Principales

- **Atención Continua (24/7):** Cero llamadas perdidas fuera de horario laboral.
- **Formato de Horario Universal:** Tratamiento agnóstico de husos horarios locales sin desfase de agenda.
- **Filtro de Urgencias Médicas:** Identificación de casos críticos para notificación directa al especialista.
- **Confirmación Inmediata:** Notificación por correo con los detalles de la consulta al paciente y al doctor.

---

## ⚙️ Despliegue Local

1. Clona el repositorio:
   ```bash
   git clone [https://github.com/arismariamateo/asistenteIA_voz-demo.git](https://github.com/arismariamateo/asistenteIA_voz-demo.git)