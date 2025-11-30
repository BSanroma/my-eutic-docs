# MY-EUTIC: FUNCIONALIDADES Y ROADMAP PÚBLICO

**Versión Pública - Noviembre 2025**

*Documento que describe las funcionalidades implementadas, en desarrollo y futuras de My-Eutic. Transparencia total sobre nuestro roadmap tecnológico.*

---

## 📋 ÍNDICE

1. [Resumen Ejecutivo](#resumen-ejecutivo)
2. [Funcionalidades Implementadas](#funcionalidades-implementadas)
3. [Funcionalidades en Desarrollo](#funcionalidades-en-desarrollo)
4. [Funcionalidades Futuras](#funcionalidades-futuras)
5. [Roadmap Público](#roadmap-público)
6. [Stack Tecnológico](#stack-tecnológico)
7. [Cómo Contribuir](#cómo-contribuir)

---

## RESUMEN EJECUTIVO

My-Eutic es una plataforma educativa que combina la metodología socrática clásica con inteligencia artificial avanzada. Nuestro objetivo es transformar el aprendizaje en una experiencia dialógica que desarrolle el pensamiento crítico y la autonomía intelectual.

### Estado del Proyecto

- **Technology Readiness Level (TRL):** 7 (Demostración en entorno operativo)
- **MVP Funcional:** ✅ Sí (mvp.my-eutic.org/classroom)
- **Pilotos Activos:** 2 centros educativos (fundaciones)
- **Usuarios Actuales:** 50+ estudiantes en fase piloto

### Estadísticas de Funcionalidades

| Estado | Cantidad | Porcentaje |
| :--- | ---: | ---: |
| ✅ Implementado | 15 | 33% |
| 🔄 En Desarrollo | 20 | 44% |
| 📅 Futuro | 10 | 23% |
| **TOTAL** | **45** | **100%** |

---

## FUNCIONALIDADES IMPLEMENTADAS

### 1. Motor Socrático Base

El corazón de My-Eutic: un sistema de diálogo que guía a los estudiantes mediante preguntas estratégicas, sin dar respuestas directas.

#### ✅ Diálogo Socrático Conversacional
- Preguntas adaptativas que se ajustan a las respuestas del estudiante
- Memoria conversacional extendida (900K+ tokens)
- Generación de preguntas en tiempo real
- Conversaciones coherentes y contextuales

**Tecnología:** Google Gemini API + Prompts pedagógicos personalizados

#### ✅ Memoria Conversacional Extendida
- Mantiene contexto de conversaciones largas
- Recuperación rápida de historial
- Optimización de tokens para máxima eficiencia

#### ✅ Generación de Preguntas Adaptativas
- Las preguntas se adaptan según el nivel de respuesta
- Basadas en Bloom's Taxonomy
- Progresión de complejidad automática

---

### 2. Integración y Autenticación

Conexión sin fricciones con los sistemas educativos existentes.

#### ✅ Integración LTI 1.3
- Compatible con Moodle, Canvas, Google Classroom, Blackboard
- Estándar IMS Global Learning Tools Interoperability
- Instalación en minutos, sin infraestructura adicional

#### ✅ Single Sign-On (SSO)
- Acceso con credenciales del LMS
- Sin necesidad de nuevas contraseñas
- Sesiones seguras con JWT tokens

#### ✅ Sincronización Automática de Notas
- Grade passback automático al LMS
- Sincronización en tiempo real
- Reintento automático en caso de error

---

### 3. Interfaz de Usuario

Dashboards intuitivos para estudiantes y profesores.

#### ✅ Dashboard de Estudiante
- Acceso a actividades asignadas
- Historial de sesiones
- Progreso visual
- Notificaciones

#### ✅ Dashboard de Profesor
- Creación de actividades
- Visualización de analíticas
- Gestión de estudiantes
- Exportación de datos

#### ✅ Interfaz de Chat Conversacional
- Interacción en tiempo real
- Historial persistente
- Indicadores de estado
- Bloqueo de copiar/pegar (en áreas críticas)

---

### 4. Seguridad y Privacidad

Cumplimiento total de estándares de protección de datos.

#### ✅ Base de Datos PostgreSQL (Supabase)
- Almacenamiento seguro y escalable
- Row Level Security (RLS)
- Backups automáticos
- Encriptación en reposo

#### ✅ Cifrado de Datos en Tránsito
- TLS 1.3 para todas las comunicaciones
- HTTPS obligatorio
- Headers de seguridad

#### ✅ Cumplimiento RGPD
- Pseudo-anonimización de datos
- Consentimiento explícito
- Derecho al olvido implementado
- Transparencia total

---

### 5. Generación de Informes

Análisis automático del proceso de aprendizaje.

#### ✅ Generación de Informes de Aprendizaje
- Análisis de conversación
- Extracción de evidencias de razonamiento
- Informes en PDF
- Puntuaciones de profundidad y claridad

#### ✅ Mapeo de Competencias LOMLOE
- Alineación automática con 8 competencias clave
- Evaluación de CCL, STEM, CPSAA, CD, CC, etc.
- Evidencias trazables
- Cumplimiento normativo

#### ✅ Código de Trazabilidad Único
- UUID único por tarea
- Infalsificable
- Verificable públicamente
- Auditoría completa

---

## FUNCIONALIDADES EN DESARROLLO

### 1. Adaptación a Necesidades Educativas Especiales (NEE)

Inclusión real mediante adaptación automática.

#### 🔄 Detección Automática de NEE
- Sistema ML que identifica el perfil del estudiante
- Cuestionario inicial + análisis de comportamiento
- Perfiles detectables: TDAH, Dislexia, TEA, Discalculia, etc.
- **Timeline:** Q2 2026

#### 🔄 Adaptaciones Visuales
- Tamaño de letra ajustable (12px - 32px)
- Modo de lectura fácil
- Alto contraste
- Fuentes optimizadas para dislexia
- **Timeline:** Q2 2026

#### 🔄 Adaptaciones de Interacción
- Tiempos de respuesta configurables
- Fragmentación de tareas en pasos pequeños
- Refuerzo motivacional automático
- **Timeline:** Q2-Q3 2026

#### 🔄 Adaptaciones Lingüísticas
- Simplificación de sintaxis (para dislexia)
- Lenguaje literal y estructurado (para TEA)
- Desglose de pasos matemáticos (para discalculia)
- **Timeline:** Q3 2026

---

### 2. Verificación de Identidad y Integridad Académica

Garantizar que el trabajo es del estudiante.

#### 🔄 Verificación Biométrica Pasiva
- Análisis del patrón de escritura (keystroke dynamics)
- No invasivo, continuo
- Detección de anomalías
- **Estado:** 60% completado
- **Timeline:** Q3 2026

#### 🔄 Detección de Intentos de Copia
- Detección de copiar/pegar
- Identificación de respuestas generadas por IA
- Análisis de coherencia
- Tasa de precisión: >95%
- **Timeline:** Q2 2026

#### 🔄 Análisis de Coherencia
- Verificación de consistencia con perfil del estudiante
- Detección de cambios abruptos de nivel
- Validación contextual
- **Timeline:** Q3 2026

---

### 3. Asistente IA para Docentes

Herramientas inteligentes para mejorar la enseñanza.

#### 🔄 Análisis de Tendencias de Clase
- Identificación de patrones de dificultad
- Conceptos problemáticos
- Comparación con clases anteriores
- **Timeline:** Q3 2026

#### 🔄 Generación Automática de Tareas
- Creación de actividades basadas en objetivos pedagógicos
- Validación automática de calidad
- Plantillas personalizables
- **Timeline:** Q4 2026

#### 🔄 Detección Temprana de Dificultades
- Alertas automáticas para estudiantes en riesgo
- Recomendaciones de intervención
- Notificaciones en tiempo real
- **Timeline:** Q3 2026

#### 🔄 Recomendaciones Pedagógicas
- Sugerencias basadas en datos
- Recursos adicionales automáticos
- Seguimiento de efectividad
- **Timeline:** Q4 2026

---

### 4. Analíticas Avanzadas

Datos profundos sobre el aprendizaje.

#### 🔄 Dashboard de Analíticas
- Visualización de datos de clase
- Gráficos interactivos
- Filtrado y drill-down
- Exportación de datos
- **Timeline:** Q3 2026

#### 🔄 Seguimiento del Progreso Conceptual
- Medición del dominio de conceptos
- Mapeo de relaciones entre conceptos
- Predicción de dificultades futuras
- **Timeline:** Q3 2026

#### 🔄 Visualización de Patrones de Aprendizaje
- Curva de aprendizaje individual
- Fortalezas y debilidades
- Comparación con compañeros (percentil)
- **Timeline:** Q2 2026

#### 🔄 Exportación de Datos
- PDF, Excel, CSV, JSON
- Informes personalizables
- Batch processing
- **Timeline:** Q2 2026

---

## FUNCIONALIDADES FUTURAS

### 1. Expansión de Integraciones

#### 📅 Google Classroom Avanzada
- Sincronización bidireccional
- Notificaciones integradas
- **Timeline:** 2026

#### 📅 Microsoft Teams
- Integración nativa
- Teams app
- **Timeline:** 2027

#### 📅 Aplicación Móvil
- iOS y Android nativos
- React Native
- **Timeline:** 2027

---

### 2. Mejoras de IA

#### 📅 Modelo de IA Propio
- Desarrollo de modelo especializado en educación socrática
- Mayor control y privacidad
- Reducción de costos
- **Timeline:** 2027

#### 📅 Detección de Emociones
- Análisis del estado emocional del estudiante
- Adaptación de tono
- Intervención de apoyo
- **Timeline:** 2027

#### 📅 Generación de Preguntas Contextuales
- Preguntas dinámicamente generadas
- Mayor relevancia pedagógica
- **Timeline:** 2026

---

### 3. Expansión Geográfica

#### 📅 Soporte Multiidioma
- Español, Catalán, Inglés, Francés, Portugués
- Interfaz completamente localizada
- **Timeline:** 2027

#### 📅 Mercados LATAM
- Adaptación para América Latina
- Cumplimiento de regulaciones locales
- **Timeline:** 2027

---

## ROADMAP PÚBLICO

### Q2 2026

**Lanzamiento Comercial v1.0**
- Modo lectura fácil
- Adaptación de tamaño de letra
- Adaptación de tiempos de respuesta
- Visualización de patrones de aprendizaje
- Exportación de datos
- Detección de intentos de copia

**Hitos:**
- ✅ Finalización de pilotos
- ✅ Análisis de resultados
- ✅ Iteración basada en feedback
- ✅ Lanzamiento comercial

---

### Q3 2026

**Inclusión Completa y Verificación**
- Detección automática de NEE
- Simplificación de sintaxis (Dislexia)
- Lenguaje literal (TEA)
- Análisis de coherencia
- Análisis de tendencias de clase
- Detección temprana de dificultades
- Seguimiento del progreso conceptual
- Verificación biométrica pasiva
- Refuerzo motivacional

**Hitos:**
- ✅ Soporte para 8+ perfiles de NEE
- ✅ Tasa de detección de copia >95%
- ✅ Dashboard de analíticas funcional

---

### Q4 2026

**Asistente IA y Expansión**
- Desglose de pasos matemáticos
- Generación automática de tareas
- Recomendaciones pedagógicas
- Integración Google Classroom avanzada
- Generación de preguntas contextuales

**Hitos:**
- ✅ Asistente IA para docentes completo
- ✅ Preparación para Erasmus+ KA220

---

### 2027

**Escalabilidad Global**
- Modelo de IA propio
- Detección de emociones
- Aplicación móvil (iOS/Android)
- Integración Microsoft Teams
- Soporte multiidioma
- Expansión LATAM
- Colaboración en tiempo real

**Hitos:**
- ✅ Presencia en 5+ países europeos
- ✅ 10,000+ estudiantes activos
- ✅ Estándar de oro para evaluación de competencias

---

## STACK TECNOLÓGICO

### Frontend

- **React 18+** - Framework UI moderno
- **TypeScript** - Tipado estático
- **Tailwind CSS** - Diseño responsive
- **Shadcn/ui** - Componentes accesibles
- **Recharts** - Visualización de datos

### Backend

- **Supabase** - Base de datos PostgreSQL gestionada
- **Edge Functions** - Lógica serverless
- **Row Level Security** - Seguridad a nivel de datos
- **PostgreSQL 14+** - Base de datos relacional

### Inteligencia Artificial

- **Google Gemini API** - Modelo de lenguaje avanzado
- **Prompts pedagógicos** - Diseñados por educadores
- **Context management** - Memoria conversacional eficiente

### Integración

- **LTI 1.3** - Estándar IMS Global
- **OAuth 2.0** - Autenticación segura
- **Grade passback** - Sincronización automática de notas

### DevOps

- **GitHub** - Control de versiones
- **Vercel** - Hosting frontend
- **Supabase Cloud** - Hosting backend
- **GitHub Actions** - CI/CD

---

## PRINCIPIOS DE DESARROLLO

### 1. Pedagogía Primero
Todas las decisiones técnicas están guiadas por la pedagogía. La tecnología sirve al aprendizaje, no al revés.

### 2. Inclusión por Defecto
No es una "característica especial". La adaptación a NEE está integrada en el core del sistema.

### 3. Privacidad y Seguridad
- RGPD compliant
- Datos encriptados
- Sin comercialización de datos
- Transparencia total

### 4. Transparencia
- Código abierto (documentación)
- Roadmap público
- Comunicación clara con usuarios
- Feedback constante

### 5. Escalabilidad Responsable
- Crecimiento sostenible
- Calidad antes que velocidad
- Impacto educativo medible
- Sostenibilidad económica

---

## CÓMO CONTRIBUIR

### Para Educadores

¿Tienes ideas sobre cómo mejorar My-Eutic?
- Abre un issue en GitHub
- Participa en discusiones
- Proporciona feedback de tus estudiantes

### Para Desarrolladores

Buscamos contribuidores en:
- Frontend (React/TypeScript)
- Backend (Edge Functions/PostgreSQL)
- ML/AI (detección de NEE, análisis de coherencia)
- Documentación

**Pasos:**
1. Fork el repositorio
2. Crea una rama para tu feature
3. Envía un pull request
4. Participa en la revisión

### Para Investigadores

My-Eutic es una plataforma para investigación en educación:
- Metodología socrática + IA
- Pensamiento crítico
- Inclusión educativa
- Evaluación de competencias

Contacta con nosotros para colaboraciones de investigación.

---

## CONTACTO Y SOPORTE

- 📧 **Email:** contact@my-eutic.org
- 🐛 **Issues:** [GitHub Issues](https://github.com/BSanroma/my-eutic-docs/issues)
- 💬 **Discusiones:** [GitHub Discussions](https://github.com/BSanroma/my-eutic-docs/discussions)
- 🌐 **Web:** https://my-eutic.org

---

## LICENCIA

Esta documentación está disponible bajo licencia MIT.

---

## AGRADECIMIENTOS

My-Eutic es posible gracias a:
- Nuestros educadores colaboradores
- Los estudiantes de los pilotos
- La comunidad de código abierto
- Google Gemini API
- Supabase

---

**Última actualización:** Noviembre 2025

*My-Eutic: Transformando la educación mediante diálogos socráticos impulsados por inteligencia artificial.*
