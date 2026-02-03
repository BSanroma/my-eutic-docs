# 🔌 Guía de Integración LTI 1.3 - My-Eutic

Esta guía detalla cómo conectar My-Eutic con cualquier Learning Management System (LMS) compatible con el estándar **LTI 1.3 Advantage**.

## ⚡ Registro Dinámico (Recomendado)

My-Eutic soporta **IMS Global Dynamic Registration**, lo que convierte la configuración en un proceso de segundos. 

### En Moodle 4.x:
1. Ve a **Administración del sitio** > **Extensiones** > **Herramientas externas** > **Gestionar herramientas**.
2. Pega la seguinte URL en el campo "URL de la herramienta":
   `https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/lti/config`
3. Haz clic en **Añadir LTI Advantage**. ¡Listo!

---

## 🛠️ Configuración Manual (Canvas, Blackboard, etc.)

Si tu plataforma no soporta el registro dinámico, utiliza los parámetros técnicos certificados:

| Parámetro | Valor |
|-----------|-------|
| **OIDC Login URL** | `https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/lti/login` |
| **Redirect URL** | `https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/lti/launch` |
| **JWKS URL** | `https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/jwks` |
| **Deep Linking** | Habilitado (Permite selección de tareas específicas) |

---

## 🔄 Arquitectura de Conexión

```mermaid
graph LR
    subgraph LMS (Moodle/Canvas)
        A[Actividad My-Eutic]
    end
    subgraph My-Eutic Cloud
        B[Connector]
        C[OIDC Auth]
        D[App Interface]
    end
    
    A -->|1. Launch| B
    B -->|2. OIDC Check| C
    C -->|3. Signed JWT| B
    B -->|4. Secure Session| D
```

## 💎 Ventajas de LTI 1.3 Advantage
- **Provisión Automática**: No hay que crear cuentas. El alumno entra y el sistema detecta su perfil y necesidades (NEE).
- **Grade Passback**: Comunicación de resultados directa al libro de calificaciones del LMS.
- **Deep Linking**: El profesor puede asignar una tarea socrática específica a una actividad concreta del curso.

---

<div align="center">
  <p>Para soporte técnico avanzado, abre un <a href="https://github.com/BSanroma/my-eutic-docs/issues">Issue en GitHub</a>.</p>
</div>
