# 📅 Roadmap Técnico y de Madurez - My-Eutic

## Estado técnico actualizado (Noviembre 2025)

- **MVP funcional** desplegado e integrado vía LTI 1.3 con Moodle y Canvas.
- **Adaptaciones curriculares** (LOMLOE) y NEE completadas para secundaria y bachillerato.
- **Infraestructura cloud escalable:** Supabase + Edge Functions + event sourcing + RLS.
- **Trazabilidad y reporting automáticos** del razonamiento crítico del estudiante.
- **Documentación pública y modular** preparada para onboarding de CTOs y equipos.

---

## Aprovechabilidad y estructura del código

| Categoría                     | % Aprovechable | Estado actual                          |
|-------------------------------|:--------------:|----------------------------------------|
| Arquitectura y diseño         |       90%      | FSM, event sourcing, modularidad       |
| Backend (Edge Functions)      |       75%      | Lógica sólida, necesita test/rational. |
| Base de datos (Schema + RLS)  |       85%      | Políticas ya validadas, pendiente tuning. |
| Frontend (Componentes)        |       40%      | Requiere refactor de auto-generados    |
| Documentación técnica         |       70%      | Cobertura buena, falta API docs completa |
| Testing                       |       20%      | Básico, ampliar cobertura necesaria    |

**Promedio ponderado:**  
- **~63-64% del código y estructura listos para producción y migración directa**
- **~36-37% pendiente de refactor controlado** (mayoritariamente frontend y test suite)

---

## Hitos alcanzados

- Separación clara entre código **production-ready**, **refactor** y **legacy**
- Quick wins de arquitectura, documentación y seguridad aplicados:
  - Tipos/contratos centralizados
  - Limpieza de configuraciones y edge functions
  - Nuevo ROADMAP técnico público
  - Guías y documentación para cada perfil

---

## Fases próximas del roadmap

1. **Audit y limpieza (Q4 2025)**
   - Refactor frontend y componentes auto-generados
   - Mejora de cobertura de tests y QA técnico

2. **Refactor core y hardening (Q1 2026)**
   - Modularización avanzada de UI y hooks
   - Integración de tests E2E y benchmarks de performance
   - Auditoría de seguridad en edge functions y RLS

3. **Expansión funcional y visual (Q1-Q2 2026)**
   - Nuevos ejercicios adaptativos y dashboards docentes
   - Creación de manuales visuales y recursos multimedia
   - Onboarding para partners y centros piloto

4. **Despliegue producción y escalado (Q2 2026)**
   - Roll-out a instituciones europeas/universidades
   - Integración con reporting institucional y homologación

---

## Estrategia de madurez y diferenciación

- **Transparencia técnica:** Todo el estado, buenas prácticas y deuda técnica visibles y documentados.
- **Escalabilidad:** Arquitectura y backend preparados para crecimiento incremental sin reescritura radical.
- **Apertura:** Facilidad de onboarding para CTOs, talento y partners sectoriales.
- **Valor pedagógico:** Alineado con estándares curriculares y necesidades reales del aula europea.
- **Seguridad y privacidad:** RGPD/LOPD; datos siempre bajo control institucional.

---

## Recomendaciones y visión

El proyecto está listo para afrontar fases de refactor y crecimiento controlado, con una base técnica robusta y progresiva.  
La madurez es superior a la media de proyectos EdTech en fase MVP y la estructura modular permite mejoras rápidas y seguras.


Última actualización: Noviembre 2025
