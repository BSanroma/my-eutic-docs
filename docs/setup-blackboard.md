# 🖤 Guía de Configuración: My-Eutic + Blackboard Learn (LTI 1.3)

> **Tiempo estimado:** 2-3 minutos  
> **Requisitos:** Permisos de Administrador del Sistema en Blackboard Learn Ultra o Original  
> **Integración oficial:** Registrado en **Anthology Developer Network**

---

## 📋 Resumen del Proceso

```text
1. Acceder al Panel de Administrador de Blackboard > Proveedores de herramientas LTI
2. Registrar la herramienta LTI 1.3 usando el Application ID oficial de My-Eutic
3. Aprobar la herramienta y activar el acceso a cursos
4. Copiar el Deployment ID generado y enviarlo a My-Eutic
5. Los docentes ya pueden añadir My-Eutic en cualquier contenido de curso
```

---

## 🔑 Credenciales Oficiales de My-Eutic

Blackboard Learn no requiere configurar URLs complejas a mano. My-Eutic dispone de un **Application ID global certificado en Anthology**:

```text
Application ID oficial: 60cd6f5c-8f2d-40aa-9ab8-1e6be94223f4
```

---

## Paso 1: Acceder al Panel de Administrador

1. Inicia sesión en Blackboard Learn con tu cuenta de **Administrador del Sistema**.
2. En la barra de navegación superior o menú lateral, entra en el **Panel del Administrador** (*Administrator Panel*).
3. En la columna de **Integraciones de Cloud** (*Cloud Integrations*), haz clic en **Proveedores de herramientas LTI** (*LTI Tool Providers*).

---

## Paso 2: Registrar la Herramienta LTI 1.3

1. En la barra de herramientas superior, haz clic en el botón **Registrar herramienta LTI 1.3** (*Register LTI 1.3 / Advantage Tool*).
2. En el formulario que se abre, localiza el campo **ID de la aplicación** (*Client ID / Application ID*).
3. Pega el código oficial de My-Eutic:
   ```text
   60cd6f5c-8f2d-40aa-9ab8-1e6be94223f4
   ```
4. Haz clic en **Enviar** (*Submit*).

---

## Paso 3: Confirmar Parámetros y Obtener el Deployment ID

Tras pulsar Enviar, Blackboard se conectará directamente a la red central de Anthology y cargará automáticamente:
- El nombre: `My-Eutic`
- Los endpoints de JWKS (`https://developer.anthology.com/.well-known/jwks.json`), OIDC Login y Launch.

En esta pantalla debes revisar y configurar:

1. **Estado de la herramienta (*Tool Status*):** Asegúrate de que esté marcado como **Aprobado** (*Approved*).
2. **Acceso a cursos (*Course / Organization Access*):**
   - Marca la opción **Permitir el acceso a esta herramienta en los cursos**.
3. **Campos de usuario enviados:**
   - Marca: **Nombre**, **Dirección de correo electrónico** y **Rol en el curso** (necesarios para que el informe socrático individual identifique correctamente las intervenciones del estudiante y genere la rúbrica docente).
4. **Copiar el Deployment ID:**
   - En la parte superior de la página (o junto a los datos del proveedor), verás un identificador único llamado **Deployment ID** (por ejemplo: `8b7c6d5e-4f3a-2b1c-0d9e-8f7a6b5c4d3e`).
   - **Copia este Deployment ID**.
5. Haz clic en **Enviar** (*Submit*) para guardar.

---

## Paso 4: Notificar a My-Eutic

Responde al correo de activación que has recibido de My-Eutic indicando el **Deployment ID** generado en el Paso 3 y el nombre de vuestra universidad/institución. 

Nuestro equipo activará la vinculación en el cluster y la herramienta quedará 100% operativa para todos los docentes de vuestro campus.

---

## Paso 5: Cómo usan los docentes My-Eutic en Blackboard

Una vez aprobada la herramienta a nivel institucional:

1. El docente entra en cualquier curso de Blackboard.
2. En el área de **Contenido del curso**, hace clic en **+** > **Crear** > **Herramienta de enseñanza con conexión LTI** (*Teaching Tool with LTI connection*).
3. Selecciona **My-Eutic** de la lista de herramientas autorizadas.
4. Puede asignar una tarea socrática concreta del catálogo o diseñar un reto personalizado.
5. Los estudiantes hacen clic y entran en la conversación socrática en tiempo real con Single Sign-On directo.
