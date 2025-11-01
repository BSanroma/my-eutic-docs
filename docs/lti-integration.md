# 🔌 Integración LTI 1.3 - My-Eutic

My-Eutic se integra de forma sencilla y segura con cualquier LMS (Moodle, Canvas, Google Classroom…) mediante el estándar internacional LTI 1.3 (IMS Global).

## ¿Qué es LTI?

- **Learning Tools Interoperability (LTI)** es el estándar mundial para integración de herramientas educativas.
- Permite que My-Eutic funcione como un recurso externo seguro, sin instalaciones complicadas ni intercambio de datos sensibles.

## Pasos para integrar My-Eutic

1. **Accede a la configuración de recursos externos** en tu LMS (Moodle, Canvas, etc.).
2. **Añade “My-Eutic” como herramienta LTI 1.3**.
   - Solicita los datos de registro (URL, ClientID, Public Key) al equipo de My-Eutic, si no están disponibles públicamente.
3. **Configura los permisos**:
   - Acceso a datos básicos de usuario y de curso.
   - Sincronización automática de calificaciones (grade passback).
4. **Prueba la integración**:
   - Crea una actividad My-Eutic y verifica el acceso docente/alumno.
   - Revise que los informes y evidencias se vinculan correctamente al curso/actividad.
5. **Soporte y personalización**:
   - Personaliza la actividad según asignatura, nivel y objetivos didácticos.

## LMS compatibles

- **Moodle** (v3.x, 4.x)
- **Canvas LMS**
- **Google Classroom** (mediante puente externo)
- **itslearning, Blackboard, OpenedX…**  
  (Consultar disponibilidad local)

## Seguridad y privacidad en la integración

- Todo acceso y transferencia de datos ocurre de manera cifrada.
- My-Eutic nunca almacena credenciales ni datos sensibles fuera del LMS.
- Cumple RGPD, LOPD y mejores prácticas educativas.

## Recursos adicionales

- [Guía del Profesor](guia-profesor.md)
- [FAQ Docentes/TIC](faq.md)
- [Documentación del estándar LTI (IMS Global)](https://www.imsglobal.org/activity/learning-tools-interoperability)
- [OAI / OAuth 2.0 para autenticaciones](https://oauth.net/2/)

---

> ¿Tienes problemas con la integración? Contacta al equipo técnico o abre una incidencia en GitHub Issues.
