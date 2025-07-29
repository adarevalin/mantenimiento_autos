# 🚗 Sistema de Registro y Mantenimiento de Vehículos


> Este proyecto es una **API RESTful** construida con **Node.js + Express** y conectada a una base de datos **MongoDB**, desarrollada como solución backend para el registro de vehículos, mantenimientos y usuarios, incluyendo control de acceso por roles, autenticación segura y operaciones CRUD completas.

> Fue realizado como parte de un proyecto **freelancer**, con enfoque modular, extensible y preparado para escalar hacia aplicaciones móviles o sistemas web frontend.

---

## 📌 Tabla de Contenido

1. [Características principales](#características-principales)
2. [Tecnologías utilizadas](#tecnologías-utilizadas)
3. [Estructura del proyecto](#estructura-del-proyecto)
4. [Instalación y configuración](#instalación-y-configuración)
5. [Variables de entorno](#variables-de-entorno)
6. [Endpoints disponibles](#endpoints-disponibles)
7. [Autenticación y roles](#autenticación-y-roles)
8. [Modelo de base de datos](#modelo-de-base-de-datos)
9. [Consideraciones de diseño](#consideraciones-de-diseño)
10. [Errores comunes y manejo](#errores-comunes-y-manejo)
11. [Pruebas](#pruebas)
12. [Autor](#autor)
13. [Licencia](#licencia)

---

## 🎯 Características Principales

✅ Registro e inicio de sesión de usuarios  
✅ Autenticación segura mediante tokens JWT  
✅ Control de acceso basado en **roles** (admin/usuario)  
✅ Gestión de vehículos y sus datos técnicos  
✅ Registro de mantenimientos por vehículo  
✅ CRUD completo para usuarios, vehículos y mantenimientos  
✅ Conexión y persistencia con MongoDB  
✅ Estructura MVC limpia y escalable  
✅ Protección de rutas mediante middleware  
✅ CORS configurado para ambientes de desarrollo y producción  
✅ Preparado para ser desplegado en Render o similar

---

## 🧰 Tecnologías Utilizadas

- **Node.js**: entorno de ejecución JavaScript para el backend.
- **Express.js**: framework ligero para APIs RESTful.
- **MongoDB**: base de datos NoSQL para almacenamiento flexible.
- **Mongoose**: ODM para modelado de datos con MongoDB.
- **JWT**: autenticación mediante JSON Web Tokens.
- **dotenv**: manejo de variables de entorno.
- **CORS**: configuración de orígenes permitidos para la API.
- **Nodemon (dev)**: recarga automática durante el desarrollo.

---

## 🗂️ Estructura del Proyecto

```bash
.
├── controllers/              # Lógica de negocio y conexión entre modelo y ruta
│   ├── userController.js
│   ├── vehiculoController.js
│   └── mantenimientoController.js
│
├── midellwares/              # Autenticación, validación de roles, errores
│   ├── auth.js
│   └── checkRole.js
│
├── models/                   # Esquemas de datos (Mongoose)
│   ├── User.js
│   ├── Vehiculo.js
│   └── Mantenimiento.js
│
├── routes/                   # Endpoints agrupados por recurso
│   ├── users.js
│   ├── vehiculos.js
│   └── registroMantenimiento.js
│
├── utils/                    # Conexión a MongoDB
│   └── database.js
│
├── app.js                    # Archivo principal del servidor
├── .env                      # Variables de entorno (no subir al repo)
├── .gitignore
├── package.json
├── package-lock.json
└── README.md
