#  Numerología App - Portal Místico & Suscripciones Premium

Aplicación Full-Stack diseñada para ofrecer lecturas numerológicas personalizadas mediante Inteligencia Artificial (Google Gemini). El sistema incluye una pasarela de pagos automatizada para usuarios Premium, un motor de *scraping* para resultados de lotería y un sistema de notificaciones automatizadas por correo electrónico.

---

##  Tecnologías Principales

* **Frontend:** Vue 3 (Vite), Quasar Framework, Pinia, Axios.
* **Backend:** Node.js, Express, MongoDB (Mongoose).
* **IA & Integraciones:** Google Gemini AI, Mercado Pago SDK, Nodemailer.
* **Automatización:** Node-cron para tareas programadas.

---

##  Estructura del Proyecto

El proyecto sigue una arquitectura desacoplada con una clara separación de responsabilidades entre el cliente y el servidor.

###  Frontend (`numerologia-frontend`)
Interfaz moderna y reactiva con diseño "Cosmic".
* `src/assets/`: Recursos estáticos (logotipos y vectores SVG).
* `src/components/`: Componentes reutilizables y elementos de diseño personalizados (inputs y botones místicos).
* `src/composables/`: Lógica de estado y validación de formularios extraída (Auth, notificaciones).
* `src/layouts/`: Plantillas maestras para roles de Administrador, Usuario y vistas de Autenticación.
* `src/services/ & src/plugins/`: Configuración centralizada de Axios para comunicación con la API.
* `src/store/`: Gestión de estado global (Pinia) para sesiones y preferencias.
* `src/views/`: Páginas principales divididas por acceso:
    * **Públicas:** Login, Registro y Recuperación de contraseña.
    * **Usuario:** Dashboard (Normal/Premium), Perfil y Pasarela de pago.
    * **Admin:** Panel de gestión de usuarios, auditoría de pagos y estadísticas.

### ⚙️ Backend (`numerologia-backend`)
API RESTful robusta y escalable.
* `app.js`: Punto de entrada y configuración del servidor Express.
* `routes/`: Definición de endpoints (Usuarios, Pagos, Lecturas, Lotería).
* `controllers/`: Lógica de negocio y procesamiento de peticiones.
* `models/`: Esquemas de Mongoose para MongoDB (Lecturas, Pagos, Usuarios).
* `middlewares/`: Capas de seguridad (JWT), control de roles y sanitización de datos.
* `helpers/`: Funciones de utilidad:
    * Integración con **Google Gemini**.
    * Gestión de correos electrónicos (**Nodemailer**).
    * Procesamiento de pagos (**Mercado Pago**).
    * Algoritmos de cálculo numerológico.
* `cron/`: Tareas programadas para validación de membresías y envíos automáticos.
* `config/`: Configuraciones críticas y llaves de integración.
* `database/`: Configuración de la conexión a MongoDB Atlas.

---

##  Instalación Rápida

1.  **Clonar:** `git clone https://github.com/tu-usuario/nombre-repo.git`
2.  **Backend:** * `cd backend && npm install`
    * Configurar `.env` con credenciales de MongoDB, Gemini y Mercado Pago.
    * Ejecutar: `npm run dev`
3.  **Frontend:**
    * `cd frontend && npm install`
    * Ejecutar: `quasar dev`

---

## ☁️ Producción

La aplicación se encuentra desplegada y operativa en:
🔗 **[https://appnumerologia.onrender.com/#/login](https://appnumerologia.onrender.com/#/login)**

---

##  Autor
* **Aprendiz SENA ADSO** - *Desarrollo Full-Stack*
* Colaboradores: Jefferson Rojas
