# 🔒 Seguridad y Privacidad (Data Sovereignty)

En My-Eutic, la privacidad de los datos educativos no es una opción, es el cimiento de nuestra plataforma. Cumplimos con las regulaciones más estrictas (RGPD, COPPA, FERPA).

## 🛡️ Cumplimiento RGPD (GDPR)

- **Minimización de Datos**: Solo solicitamos los datos imprescindibles para el proceso educativo (nombre, email institucional proporcionado por el LMS).
- **Derechos ARCO**: Implementamos flujos automatizados para el acceso, rectificación, cancelación y oposición de datos por parte de los usuarios.
- **Firmas Digitales de Confidencialidad**: Gestionamos la aceptación de términos y NDAs de forma centralizada con auditoría (IP, User-Agent, Timestamp).

## 🔐 Blindaje Técnico

### Row Level Security (RLS)
Nuestra base de datos PostgreSQL aplica seguridad a nivel de fila. Esto significa que, incluso en caso de fallo en el código de la aplicación, la base de datos prohíbe el acceso a datos que no pertenecen al usuario autenticado. Tenemos más de **125 políticas activas** para garantizar este aislamiento.

### Cifrado
- **En Tránsito**: Todas las comunicaciones utilizan TLS 1.3.
- **En Reposo**: Los datos se almacenan cifrados mediante algoritmos AES-256.

### Vault y Secretos
Utilizamos almacenes de secretos certificados para gestionar las claves criptogáficas de la integración LTI 1.3, asegurando que nunca viajan en el código ni se exponen en logs.

## 🏫 Gobernanza para Instituciones

Los administradores de centros educativos tienen control total sobre los datos de su institución:
- Gestión selectiva de accesos por cursos o departamentos.
- Auditoría de uso y accesos.
- Posibilidad de borrado completo tras la finalización del contrato o proyecto piloto.

---

## 🤖 Privacy-by-Design en el Motor de IA

Este es uno de los compromisos técnicos más importantes de My-Eutic para los centros educativos que integran la plataforma via **LTI 1.3**.

### El principio
Los modelos de IA de Google Gemini que analizan las conversaciones para generar informes pedagógicos **nunca reciben datos personales identificables (PII)**. Los nombres de alumnos, nombres de profesores y emails son datos que los centros educativos nos ceden bajo confianza; no los transmitimos a APIs externas de procesamiento.

### Cómo funciona
- Los **prompts enviados a Gemini** contienen únicamente el contenido pedagógico de la conversación y etiquetas de contexto anónimas (ej: "Alumno con NEE: Dislexia").
- Los informes generados por la IA son vinculados internamente con el alumno real utilizando **IDs internos de Supabase**, sin que el nombre haya viajado fuera del entorno seguro.
- Las **Necesidades Educativas Especiales** se envían como etiquetas pedagógicas de contexto (para que la IA adapte su evaluación), pero nunca vinculadas al nombre real del alumno.

### Qué significa para tu centro
Ante cualquier auditoría de privacidad o inspección de la Agencia de Protección de Datos, My-Eutic puede garantizar que **ningún nombre de alumno ni dato personal identificable ha abandonado el entorno de Supabase** para ser procesado por sistemas de IA de terceros.

