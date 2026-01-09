# Guía de Integración LTI 1.3 - My-Eutic

Esta guía detalla cómo integrar My-Eutic en tu entorno de aprendizaje (LMS) compatible con LTI 1.3 (Moodle, Canvas, Blackboard, etc.).

## 🚀 Configuración Rápida (1-Click Setup)

My-Eutic soporta el estándar **IMS Global Dynamic Registration**. Esto permite configurar la herramienta de forma automática simplemente proporcionando una URL en tu LMS.

**URL de Configuración Dinámica:**
`https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/lti/config`

> [!TIP]
> En Moodle 4.x, simplemente ve a *Administración del sitio > Extensiones > Herramientas externas (LTI) > Gestionar herramientas* y pega esta URL en el campo "URL de la herramienta".

---

## 🛠️ Configuración Manual

Si tu LMS no soporta el registro dinámico, utiliza los siguientes parámetros:

| Parámetro | Valor |
|-----------|-------|
| **OIDC Login URL** | `https://api.my-eutic.org/lti/login` |
| **Redirect URL** | `https://api.my-eutic.org/lti/launch` |
| **Public Keyset URL** | `https://api.my-eutic.org/lti/keys` |
| **Deep Linking** | Soportado (Habilitar para selección de tareas) |

---

## 🔄 Flujo de Onboarding

1. **Registro**: El administrador del centro se registra en My-Eutic.
2. **Configuración**: Se vincula el `Issuer URL` del LMS con la cuenta de la institución.
3. **Lanzamiento**: Los profesores y alumnos acceden directamente desde el LMS. No es necesario crear cuentas manualmente; la provisión de usuarios es automática y segura.

---

## 🛡️ Seguridad y Privacidad

- **Autenticación RSA**: Utilizamos firmas RS256 para verificar la identidad del LMS.
- **Sin datos sensibles**: Solo procesamos los datos mínimos necesarios para el aprendizaje (nombre, email institucional).
- **Control Total**: El centro educativo mantiene el control sobre qué cursos y alumnos tienen acceso.

Para soporte técnico adicional, contacta con tu administrador de plataforma o abre un issue en nuestro repositorio de documentación.
