# Nicolás

Full-stack developer · Analista funcional TI

Estudiante de licenciatura en gestión de TI (UADE). Me especializo en construir aplicaciones web escalables que integran frontend moderno, APIs robustas e infraestructura cloud, con foco en la intersección entre decisiones técnicas y necesidades de negocio.

---

## Proyectos destacados

### Huella del fuego
*Full-stack developer — en producción · [huelladelfuego.com.ar](https://huelladelfuego.com.ar)*

Plataforma para explorar qué pasó con los terrenos afectados por incendios forestales en Argentina. Permite ver dónde ocurrió cada incendio, cómo evolucionó la vegetación en los meses y años posteriores, y si el suelo se recuperó o fue utilizado para otros fines.

Los datos provienen de satélites NASA (FIRMS) y ESA (Sentinel-2). Cualquier persona puede buscar un terreno por coordenadas y obtener una línea de tiempo visual de su historia desde el incendio hasta hoy.

Decisiones técnicas destacadas:

- Diseñé el modelo de dominio para `fire_detections` → `fire_events` → `fire_episodes` con transiciones de estado basadas en funciones de tiempo puras, sin re-chequeo de distancias.
- Clustering espacial DBSCAN con indexación hexagonal H3 (BIGINT): 10× menos almacenamiento que geometrías tradicionales, con agregaciones directas para heatmaps.
- Pipeline de análisis NDVI en 14 fases sobre Google Earth Engine: baseline construido con `qualityMosaic('NDVI')` de 365 días previos al incendio para capturar el pico anual real de vegetación.
- Arquitectura async-first: imágenes satelitales, clustering y generación de contenido delegados a workers Celery con colas separadas (`worker-fast` / `worker-gee`); la API responde 202 de forma inmediata.
- Enriquecimiento geográfico automático con PostGIS contra ~530 departamentos argentinos (datos Georef AR).

Stack: Python (FastAPI), Celery, Redis, React 19, TypeScript, Vite 7, Leaflet, Supabase (PostgreSQL/PostGIS), Google Earth Engine, NASA FIRMS, Docker Compose, Oracle Cloud ARM64, Cloudflare Pages, OCI Object Storage.

### Escalatunegocioconia
*Full-stack developer — en producción*

Plataforma de servicios de negocio con módulo de talento, catálogo de servicios digitales y blog orientado a posicionamiento orgánico.

- Arquitecté el portal de talento y servicios: modelado de datos, API REST y UI con shadcn/ui.
- Desarrollé la arquitectura de blog con rendering optimizado para SEO y estructura de rutas semánticas.
- Integré múltiples APIs externas manteniendo contratos de tipo estrictos en TypeScript.
- Stack: React, TypeScript, Vite, shadcn/ui, integraciones API, gestión de base de datos.

Subdominios en producción:

| Demo | Repo | Descripción |
|---|---|---|
| [creador-contenido.escalatunegocioconia.com](https://creador-contenido.escalatunegocioconia.com) | [remix-of-personal-blog](https://github.com/Nicolasgh91/remix-of-personal-blog) | Blog SPA para creador de contenido — React 18, React Router 6, TanStack Query, shadcn/ui |
| [template-pyme.escalatunegocioconia.com/productos](https://template-pyme.escalatunegocioconia.com/productos) | [template-pyme](https://github.com/Nicolasgh91/template-pyme) | Landing para pyme — demo panadería artesanal |
| [template-pyme.escalatunegocioconia.com/servicios](https://template-pyme.escalatunegocioconia.com/servicios) | [template-pyme](https://github.com/Nicolasgh91/template-pyme) | Landing para pyme — demo estudio contable |

---

## Stack técnico

**Frontend** ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat-square&logo=typescript&logoColor=white) ![Vite](https://img.shields.io/badge/Vite-B73BFE?style=flat-square&logo=vite&logoColor=FFD62E) ![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square&logo=shadcnui&logoColor=white) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)

**Backend** ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=spring&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-025E8C?style=flat-square)

**Infraestructura** ![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white) ![PostGIS](https://img.shields.io/badge/PostGIS-336791?style=flat-square) ![Cloudflare Workers](https://img.shields.io/badge/Cloudflare_Workers-F38020?style=flat-square&logo=cloudflare&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white) ![Oracle Cloud](https://img.shields.io/badge/Oracle_Cloud-F80000?style=flat-square&logo=oracle&logoColor=white) ![Google Cloud](https://img.shields.io/badge/Google_Cloud-4285F4?style=flat-square&logo=google-cloud&logoColor=white)

**Testing** ![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white)

**Metodologías** ![Kanban](https://img.shields.io/badge/Kanban-0052CC?style=flat-square) ![Scrum](https://img.shields.io/badge/Scrum-00A98F?style=flat-square) ![Design Thinking](https://img.shields.io/badge/Design_Thinking-E23D28?style=flat-square)

---

## Formación y experiencia de base

- Licenciatura en gestión de TI — UADE (en curso)
- Implementación de API REST con Java, Spring Boot, Maven e Hibernate
- Procesamiento de datos con Python (UTN)
- Resolución continua de problemas algorítmicos en HackerRank

---

## Contacto

- Correo: nicolasgabh33@gmail.com
- LinkedIn: [linkedin.com/in/nicolasghruszczak](https://www.linkedin.com/in/nicolasghruszczak/)
- Portfolio: [https://www.escalatunegocioconia.com/](https://github.com/Nicolasgh91/portfolio)
