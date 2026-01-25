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
