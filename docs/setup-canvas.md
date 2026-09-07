# 🎨 Guía de Configuración: My-Eutic + Canvas LMS (LTI 1.3)

> **Tiempo estimado:** 3-5 minutos  
> **Requisitos:** Permisos de Administrador de Cuenta (Root o Sub-Account Admin) en Canvas LMS  
> **Estándar:** LTI 1.3 Advantage (1EdTech Certified)

---

## 📋 Resumen del Proceso

```text
1. Crear una Developer Key (LTI Key) mediante URL en Canvas
2. Activar la clave (ON) y copiar el Client ID
3. Enviar el Client ID al equipo My-Eutic para vincular la institución
4. Instalar la aplicación en la Cuenta o Cursos usando el Client ID
5. Añadir la actividad My-Eutic a cualquier asignatura
```

---

## Paso 1: Crear la Developer Key en Canvas

1. Inicia sesión en Canvas LMS con una cuenta de **Administrador de Cuenta**.
2. En el menú de navegación global de la izquierda, haz clic en **Admin** (Administración) y selecciona tu cuenta institucional principal o subcuenta.
3. En el menú lateral de la cuenta, haz clic en **Developer Keys** (Claves de desarrollador).
4. Haz clic en el botón superior derecho **+ Developer Key** y selecciona **+ LTI Key**.

---

## Paso 2: Configurar los Parámetros LTI mediante URL (Método Rápido)

Canvas permite la autoconfiguración automática de metadatos mediante una URL JSON estándar:

1. En el formulario de la nueva clave LTI, en el campo **Method** (Método), selecciona **Enter URL**.
2. Completa los siguientes campos:

| Campo en Canvas | Valor a Introducir |
|---|---|
| **Key Name** | `My-Eutic - Pensamiento Crítico` |
| **Owner Email** | Tu correo corporativo de administrador |
| **JSON URL** | `https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/lti/config` |
| **Redirect URIs** | `https://hsevkyjsyqzzpmnvrhan.supabase.co/functions/v1/moodle-lti-connector/launch` |

3. Haz clic en **Save** (Guardar) abajo a la derecha.

> [!NOTE]
> Al pulsar Guardar mediante `JSON URL`, Canvas descargará automáticamente los endpoints seguros de OIDC Login, Public Keyset JWKS y placements para navegación de cursos y selección de actividades (Deep Linking).

---

## Paso 3: Activar la Clave y Copiar el Client ID

1. En la lista de Developer Keys, localiza la clave recién creada: **My-Eutic**.
2. En la columna **State** (Estado), cambia el conmutador de **OFF** a **ON**.
3. En la columna **Details** (Detalles), encima del botón *Show Key*, verás un número largo (generalmente de 14 a 18 dígitos, por ejemplo `10000000000042`). **Este número es vuestro Client ID**.
4. Copia este número y **responde al correo de activación de My-Eutic indicándolo**, para que nuestro equipo lo vincule de inmediato a vuestra institución en la base de datos multi-tenant.

---

## Paso 4: Instalar la App en Canvas (Por Client ID)

Una vez creada la clave, puedes hacerla disponible para toda la universidad o para subcuentas/cursos específicos:

1. Ve a **Admin** > **Settings** (Configuración) de la cuenta (o a *Settings* dentro de un curso de prueba).
2. Selecciona la pestaña **Apps** en la parte superior.
3. Haz clic en el botón **View App Configurations** (Ver configuraciones de aplicaciones) y luego en **+ App**.
4. En el desplegable **Configuration Type**, selecciona **By Client ID** (Por ID de cliente).
5. Pega el **Client ID** copiado en el Paso 3.
6. Haz clic en **Submit** (Enviar). Canvas te preguntará: *"¿Deseas instalar la herramienta My-Eutic?"*. Haz clic en **Install** (Instalar).

---

## Paso 5: Probar la Actividad en una Asignatura

1. Entra en cualquier curso donde seas docente o administrador.
2. Ve a **Assignments** (Tareas) y haz clic en **+ Assignment**.
3. En la sección **Submission Type** (Tipo de entrega), selecciona **External Tool** (Herramienta externa).
4. Haz clic en **Find** (Buscar), localiza **My-Eutic** en la lista y selecciónala.
5. Marca la casilla *"Cargar esta herramienta en una nueva pestaña"* (opcional pero recomendado para maximizar el espacio de debate).
6. Guarda y publica la tarea.
7. Al hacer clic, tanto docentes como estudiantes accederán con Single Sign-On (SSO) directo mediante LTI 1.3 sin necesidad de introducir contraseñas.
