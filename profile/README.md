# 🏗️ JobSearch Chile - Plataforma de Empleo para Construcción y Arquitectura

![Angular](https://img.shields.io/badge/Angular-19-red?logo=angular)
![NestJS](https://img.shields.io/badge/NestJS-10-E0234E?logo=nestjs)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2.5-6DB33F?logo=springboot)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-15-336791?logo=postgresql)
![Docker](https://img.shields.io/badge/Docker-24.0.7-2496ED?logo=docker)

Bienvenido a **JobSearch Chile**, la plataforma moderna para conectar profesionales y empresas del sector construcción y arquitectura. Este proyecto utiliza una arquitectura de microservicios, frontend Angular optimizado y backend escalable para ofrecer una experiencia robusta, segura y eficiente.

---

## ✨ Sobre el Proyecto

JobSearch Chile nace para digitalizar la búsqueda de empleo en el rubro de la construcción y arquitectura, facilitando la conexión entre talento y empresas, con seguridad, velocidad y una experiencia de usuario superior.

---

## 🚀 Características Principales

- **Búsqueda avanzada de empleos** por ubicación, salario y categoría
- **Registro y autenticación segura** con JWT y refresh tokens
- **Paneles personalizados** para trabajadores y empresas
- **Gestión de postulaciones y ofertas** con dashboards dedicados
- **Planes de suscripción** y facturación para empresas
- **Notificaciones y alertas de empleo**
- **Arquitectura escalable y modular** para fácil mantenimiento y crecimiento

---

## 🧩 Arquitectura General

### Microservicios

- **Spring Boot**
  - `ms-archi-gateway` (8080): Gateway API, routing inteligente
  - `ms-archi-auth-profile` (8081): Autenticación, perfiles y seguridad

- **NestJS**
  - `ms-archi-jobs-public` (3002): API pública de empleos
  - `ms-archi-job-seeker` (3003): Funcionalidades para trabajadores
  - `ms-archi-employer` (3004): Funcionalidades para empresas
  - `ms-archi-notifications` (3005): Notificaciones y alertas
  - `ms-archi-payments` (3006): Facturación y suscripciones

### Base de Datos

- **PostgreSQL 15** con esquemas por dominio (`auth`, `perfil`, `job`, `pago`, `interaccion`)
- Scripts organizados en DDL, DML y ROLLBACK para fácil gestión y migración

### Frontend Angular

- **Angular 19 + Tailwind CSS** para UI moderna y responsive
- **Lazy Loading** y **bundle splitting** para performance óptimo
- **Guards de autenticación y roles** para seguridad granular
- **SEO Ready** y mobile first

---
_Este diagrama muestra la comunicación entre el cliente Angular, el gateway y los microservicios vía gRPC._

## 📁 Estructura de Carpetas

```
frontend-naev-job-search/
└── src/app/
    ├── core/         # Servicios, guards, interceptors
    ├── shared/       # Componentes reutilizables
    └── features/
        ├── public/       # Home, búsqueda, detalles, precios, about
        ├── auth/         # Login, registro, recuperación de contraseña
        ├── job-seeker/   # Dashboard, postulaciones, perfil, favoritos
        ├── employer/     # Dashboard, publicar, gestionar, analytics
        └── admin/        # Administración (futuro)
```

---

## 🛣️ Rutas y Navegación

- **Rutas públicas:** Home, búsqueda, detalles, precios, about
- **Rutas privadas:** Paneles de trabajador y empresa (lazy loading)
- **Guards:** Autenticación, suscripción y roles

---

## 🛠️ Stack Tecnológico

- **Frontend:** Angular 19, Tailwind CSS, RxJS, Lazy Loading
- **Backend:** Spring Boot, NestJS, PostgreSQL, Redis, RabbitMQ
- **Infraestructura:** Docker, Kubernetes, Nginx, AWS/GCP

---

## 🏗️ Cómo Ejecutar el Proyecto

1. Clona el repositorio
2. Configura variables de entorno en `.env` y archivos de configuración
3. Levanta la base de datos y microservicios con Docker Compose:
   ```powershell
   docker-compose up -d
   ```
4. Instala dependencias frontend y ejecuta Angular:
   ```powershell
   cd frontend-naev-job-search
   npm install
   npm start
   ```
5. Accede a la app en [http://localhost:4200](http://localhost:4200)


## 🎯 Próximos Pasos

- Implementar guards y servicios por dominio
- Desarrollar paneles completos para trabajadores y empresas
- Integrar notificaciones y facturación
- Mejorar tests y cobertura de endpoints

---

## 💡 Ventajas de la Plataforma

- **Separación clara de responsabilidades** por dominio
- **Escalabilidad y performance** gracias a lazy loading y microservicios
- **Seguridad avanzada** con JWT, guards y roles
- **Experiencia de usuario optimizada** para dispositivos móviles y SEO

---

