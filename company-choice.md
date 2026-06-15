# Company Choice — Milestone 0

## Empresa elegida: Nexova Solutions

**Sector:** Consultoría de recursos humanos y selección de talento  
**Sede:** Valencia, España (con oficina en Miami, Florida)  
**Tamaño:** 120 empleados · ~8M USD de facturación anual

---

## Por qué elegí Nexova

He elegido Nexova Solutions porque es la empresa donde la inteligencia artificial no actúa como una herramienta de soporte periférica, sino como la ventaja competitiva central del negocio. En los tres escenarios disponibles, Nexova es la única en la que los entregables de AI Engineering — scoring de CVs, RAG sobre base de candidatos, agentes de comunicación automática, motor de recomendación formativa — son la propuesta de valor que diferencia a la empresa de sus competidores, no mejoras internas opcionales.

Como desarrollador full-stack, me interesa especialmente el reto de integrar múltiples fuentes de datos heterogéneas (ATS legacy, HubSpot, Google Workspace, Zendesk) en una arquitectura coherente que sirva a departamentos con necesidades muy distintas. Nexova presenta exactamente esa complejidad: cinco equipos con flujos de trabajo, datos y definiciones de éxito completamente diferentes, pero que comparten la misma infraestructura subyacente.

Además, el sector de RRHH y selección de talento es uno donde la automatización inteligente tiene un impacto directo y medible: reducir el tiempo de cribado de 80 CVs manuales a un ranking automatizado y explicable es algo que cualquier recruiter entiende de inmediato, y esa claridad de impacto es valiosa tanto para el desarrollo del proyecto como para presentarlo en un portfolio o una entrevista.

Finalmente, Nexova tiene sede en Valencia — el mismo mercado donde opero — lo que me permite entender el contexto cultural y de negocio B2B con mayor profundidad desde el primer día.

---

## Departamentos que encuentro más interesantes

### 1. Operaciones de Selección (negocio principal)
**Responsable:** Javier Almeida — 40 consultores de selección

Este departamento es el núcleo del negocio y el que concentra los retos de AI Engineering más sustanciosos. El proceso actual es completamente manual: cada consultor lee entre 30 y 80 CVs por proceso, el matching entre candidato y vacante depende de la intuición individual y los clientes no tienen visibilidad del estado de sus procesos en tiempo real.

Lo que me atrae de este departamento es que los datos son ricos y estructurados (CVs, descripciones de vacantes, historiales de candidatos) y los problemas son concretos y medibles: cuántos CVs se criban por hora, cuánto tiempo tarda un candidato en pasar de etapa, qué porcentaje de candidatos enviados acaban contratados. Un pipeline de scoring con RAG sobre la base de candidatos existente es exactamente el tipo de sistema que demuestra AI Engineering aplicada con criterio técnico y de negocio.

### 2. Atención al Cliente Externalizado
**Responsable:** Roberto Díaz — 30 agentes

El tiempo medio de resolución de 48 horas contra un SLA comprometido de 24 es una brecha crítica que tiene consecuencias directas en la relación con los clientes de outsourcing. La ausencia de una base de conocimiento centralizada — los agentes resuelven por experiencia y un documento Word compartido — hace que cada consulta dependa del agente que la recibe, sin consistencia ni escalabilidad.

Me interesa construir aquí el chatbot de primera línea con RAG sobre la base de conocimiento y el dashboard de soporte en tiempo real. Es un caso de uso donde el impacto se mide en horas de resolución y en porcentaje de consultas resueltas sin intervención humana — métricas claras que hablan por sí solas en un portfolio.

---

## Reto de automatización del milestone map que más me atrae

El reto que más ganas tengo de construir es el **sistema RAG sobre la base de datos de candidatos** de Operaciones de Selección.

El escenario es el siguiente: Nexova lleva doce años acumulando perfiles de candidatos en un ATS construido a principios de los 2010. Ese conocimiento existe pero es prácticamente inaccesible — un consultor que necesita "perfiles con experiencia en ventas B2B y nivel C1 de inglés" tiene que hacer búsquedas manuales imprecisas en un sistema que no fue diseñado para búsqueda semántica.

Un sistema RAG sobre esa base resuelve un problema real de negocio, demuestra dominio de embeddings, recuperación semántica y arquitectura de agentes, y genera un entregable cuyo valor el cliente entiende inmediatamente. Es el tipo de proyecto que aparece en entrevistas de trabajo y que diferencia a un AI Engineer de alguien que solo sabe llamar a una API.

---

## Mi idea de Agente de IA

**Agente de Cribado y Matching de Candidatos para Operaciones de Selección**

El agente recibiría como entrada la descripción de una vacante (texto libre o briefing estructurado del cliente) y accedería a la base de datos de candidatos de Nexova mediante búsqueda semántica vectorial.

**Qué haría:**
- Convertiría la descripción de la vacante en un embedding y realizaría una búsqueda de similitud sobre los CVs indexados.
- Generaría un ranking de los 10-15 candidatos más relevantes con una puntuación explicable (por qué encaja cada perfil, qué requisitos cumple y cuáles no).
- Redactaría automáticamente el email de contacto personalizado para cada candidato seleccionado, listo para revisión del consultor antes del envío.
- Actualizaría el estado del candidato en el pipeline en tiempo real.

**Qué información necesitaría:**
- Acceso vectorizado a la base de candidatos existente (CVs, experiencia, habilidades, idiomas, disponibilidad).
- La descripción de la vacante y los criterios de selección del cliente.
- El historial de candidatos enviados y contratados anteriormente (para mejorar el ranking con feedback real).

**Qué produciría:**
- Un ranking de candidatos con puntuación y justificación para el consultor.
- Borradores de emails de contacto personalizados.
- Actualización automática del estado en el ATS.
- Reducción del tiempo de cribado de horas a minutos por proceso.

