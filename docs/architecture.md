# 🏗️ Arquitectura Técnica - My-Eutic

Este documento describe la arquitectura técnica de My-Eutic, resaltando los componentes clave del sistema, el enfoque modular y las ventajas para integración, seguridad y escalabilidad.

---

## 🧩 Visión general de la arquitectura

- **Frontend:**  
  - React + TypeScript (modular, escalable y adaptable a distintos flows)
  - Tailwind CSS (diseño accesible, rápido y responsivo)
  - Shadcn/ui (componentes UI modernos, minimalistas, accesibles)
- **Backend:**  
  - Supabase (PostgreSQL gestionada, funciones RPC, autenticación, RLS)
  - Edge Functions (serverless, lógica de negocio crítica aislada y auditable)
  - Event Sourcing (auditoría de eventos, trazabilidad total del proceso educativo)
- **IA & Servicios:**  
  - Google Gemini AI (conversaciones y prompts personalizados orientados a aprendizaje Socrático)
  - Prompts pedagógicos propios validados por docentes

---

## 🔒 Seguridad y privacidad

- **Row Level Security (RLS)** en todas las tablas:  
  Cada estudiante, docente o admin solo accede a los datos que le corresponden.
- **Cumplimiento RGPD/LOPD**:  
  Control estricto de la información y anonimización para reporting externo.
- **Audit log:**  
  Todas las acciones sensibles quedan trazadas.

---

## 🔗 Integración externa

- **LTI 1.3 (IMS Global):**  
  Facilitada para conectar la plataforma con cualquier LMS moderno (Moodle, Canvas, etc.) sin fricción ni riesgos de seguridad.
- **OAuth 2.0:**  
  Autenticación robusta y escalable para escenarios BYOI (Bring Your Own Identity).

---

## 🛠️ Modularidad y ventajas de diseño

- **Event Sourcing + FSM**:  
  Permite trazabilidad avanzada, recuperación de estados y análisis pedagógico profundo.
- **Frontend desacoplado:**  
  Diseño por módulos y hooks: “plug-and-play” para UI/UX y mejoras rápidas.
- **Edge Functions:**  
  Distribución lógica serverless para escalabilidad real y control granular de recursos.

---

## Esquema conceptual de arquitectura

*(Añade aquí tu diagrama visual, por ejemplo `docs/assets/arquitectura.png`)*

![Diagrama de la arquitectura de My-Eutic](assets/arquitectura.png)

---

## Plan de evolución técnica

- Incrementar modularidad en frontend (microfrontend-ready)
- Refactorizar auto-generados y duplicidades
- API pública documentada (OpenAPI 3)
- Benchmarks y performance monitoring (E2E + DevOps)
- Preparar para integraciones multimodales (voz, analítica avanzada, etc.)

---

¿Quieres más detalles? Consulta la [Documentación API](api.md) o abre una discusión técnica en el repositorio.
