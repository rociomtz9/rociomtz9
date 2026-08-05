# 👋 Hola, soy Rocío Martínez
 
Estudiante de Ingeniería en Informática en la UNCA (Paraguay). Me gusta resolver problemas reales con código — es lo que me atrajo de la informática desde chica y lo que me mantiene acá.
 
---
 
## Proyectos
 
### [progreso-malla-fcyt](https://github.com/rociomtz9/progreso-malla-fcyt) · [Demo](https://malla-unca.vercel.app)
 
*Tracker de avance académico que calcula correlatividades y exporta a Excel.*
 
- **El reto:** que 84 materias con correlatividades encadenadas se resuelvan solas, sin backend y sin que los datos de nadie salgan de su dispositivo.
- **La solución:** HTML + CSS + JavaScript puro con ES modules. Cero dependencias, cero build, cero servidor. Generación de `.xlsx` con formato condicional y fórmulas, escrita íntegramente en el navegador.
- **Seguridad:** CSP restrictiva (`default-src 'none'`), HSTS, `frame-ancestors 'none'`, `Permissions-Policy` y construcción del DOM sin `innerHTML` en ningún punto. El progreso vive solo en `localStorage`.
### [vistas-english](https://github.com/rociomtz9/vistas-english) · [Demo](https://vistas-study-app.vercel.app)
 
*PWA para estudiar inglés, con ejercicios generados algorítmicamente.*
 
- **El reto:** generar actividades válidas a partir del contenido de cada lección, sin escribir ni una a mano, y garantizar que ninguna quede rota o con la respuesta a la vista.
- **La solución:** React + Vite + Supabase. Un generador que abre huecos en los diálogos cuidando de no ofrecer sinónimos como distractores, verificado con **property-based testing** (Vitest + PRNG con semilla) sobre decenas de semillas aleatorias.
- **Offline:** el progreso se guarda al instante en `localStorage` y se sincroniza con Supabase en segundo plano; una cola de pendientes reintenta lo que falle.
- **Seguridad:** Row Level Security en todas las tablas con políticas por operación (`auth.uid() = user_id`), trigger `security definer` con `search_path` fijado, CSP + HSTS + `X-Frame-Options`, y separación del contenido editorial de terceros del código publicado (el repo trae un set de lecciones de ejemplo propio, con fallo explícito si se pide el contenido real y no está).
### [javicell](https://github.com/rociomtz9/javicell)
 
*Sistema de gestión de escritorio para un taller de reparación de celulares real.*
 
- **El reto:** digitalizar un negocio que funcionaba en papel, sin perder trazabilidad de ninguna operación.
- **La solución:** Java 21 + PostgreSQL 17 con arquitectura estricta en capas (Model / DAO / Service / UI). Transacciones ACID con rollback para operaciones compuestas, soft-delete con auditoría por triggers, y reglas de negocio automatizadas (saldos, estados de reparación, garantías).
- **Seguridad:** contraseñas con BCrypt, consultas 100 % parametrizadas (sin concatenación de entrada en SQL), credenciales por variables de entorno, y sin usuarios de fábrica: el primer administrador se crea en el arranque con una clave que define el propio usuario.
### dtc_app *(repositorio privado)* · [Demo](https://dtc-diagnostico.netlify.app)
 
*Herramienta de diagnóstico de códigos de falla (DTC) para técnicos de camiones Scania.*
 
- **El reto:** buscar códigos de falla en talleres donde la conexión es intermitente.
- **La solución:** app multiplataforma en Flutter (Android, iOS, Web, Desktop) sobre PostgreSQL en la nube, con un esquema de 15 tablas que modela contexto del vehículo, síntomas, causas y procedimientos, y gestión de roles con permisos estrictos.
---
 
## Stack
 
**Lenguajes:** `Java 21` · `JavaScript (ES modules)` · `SQL` · `Dart`
 
**Frontend:** `React` · `Vite` · `Tailwind CSS` · `PWA / Service Workers` · `Flutter`
 
**Datos:** `PostgreSQL` · `Supabase (Auth, RLS, Edge Functions)`
 
**Calidad y seguridad:** `Vitest` · `property-based testing` · `Content Security Policy` · `BCrypt` · `Maven`
 
---
 
## Contacto
 
- Correo: martinezm.rocio2017@gmail.com
