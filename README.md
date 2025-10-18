# Curso de n8n con Evolution API e IA

Este repositorio contiene el material y proyectos del curso de n8n, donde aprendemos a crear flujos de automatización completos utilizando Evolution API para WhatsApp e integración con servicios de IA.

## 📋 Descripción del Curso

El curso se enfoca en enseñar cómo crear automatizaciones poderosas combinando:
- **n8n**: Plataforma de automatización de workflows
- **Evolution API**: API para integración con WhatsApp
- **Servicios de IA**: Para generar respuestas inteligentes y procesar datos

Cada workflow representa una clase o mini-proyecto desarrollado durante el curso, donde se exploran diferentes casos de uso y técnicas de automatización.

## 👨‍🏫 Información del Curso

- **Instructor**: Iván Martínez
- **Institución**: CCOL (Centro de Capacitación en Línea)
- **Modalidad**: Curso práctico de automatización

## 🏗️ Arquitectura del Proyecto

### Componentes Principales

#### n8n (Automatización)
- **Puerto**: 5678
- **Timezone**: America/Mexico_City
- **Funcionalidad**: Plataforma principal para crear y ejecutar workflows de automatización

#### Evolution API (WhatsApp Integration)
- **Puerto**: 8080
- **Versión**: v2.3.3
- **Funcionalidad**: API para conectar y automatizar WhatsApp

#### Base de Datos PostgreSQL
- **Puerto**: 5432
- **Base de datos**: evolution_db
- **Usuario**: evolution_user
- **Funcionalidad**: Almacenamiento de datos de instancias, mensajes y contactos

#### Redis (Caché)
- **Puerto**: 6379
- **Funcionalidad**: Sistema de caché para optimizar el rendimiento

## 🚀 Instalación y Configuración

### Prerrequisitos
- Docker y Docker Compose instalados
- Git para clonar el repositorio

### Pasos de Instalación

1. **Clonar el repositorio**
```bash
git clone <url-del-repositorio>
cd n8n_curso
```

2. **Iniciar n8n**
```bash
docker-compose up -d
```

3. **Iniciar Evolution API**
```bash
cd evolutionAPI
docker-compose up -d
```

4. **Acceder a las aplicaciones**
- n8n: http://localhost:5678
- Evolution API: http://localhost:8080

## 📁 Estructura del Proyecto

```
n8n_curso/
├── docker-compose.yml          # Configuración de n8n
├── evolutionAPI/
│   ├── docker-compose.yml      # Configuración de Evolution API
│   └── .env                    # Variables de entorno
└── README.md                   # Este archivo
```

## ⚙️ Configuración

### Evolution API
La configuración se encuentra en `evolutionAPI/.env`:
- **Autenticación**: Clave API personalizada
- **Logs**: Configurados para debugging completo
- **Base de datos**: PostgreSQL con guardado automático de datos
- **Caché**: Redis habilitado para mejor rendimiento

### n8n
- **Timezone**: Configurado para México (America/Mexico_City)
- **Runners**: Habilitados para ejecución distribuida
- **Persistencia**: Datos almacenados en volumen Docker

## 🎯 Casos de Uso del Curso

Durante el curso desarrollamos workflows que cubren:
- Automatización de respuestas en WhatsApp
- Integración con servicios de IA para generar contenido
- Procesamiento de mensajes y datos
- Flujos de trabajo complejos con múltiples integraciones
- Gestión de contactos y conversaciones

## 🔧 Comandos Útiles

### Gestión de Contenedores
```bash
# Iniciar todos los servicios
docker-compose up -d

# Ver logs
docker-compose logs -f

# Detener servicios
docker-compose down

# Reiniciar un servicio específico
docker-compose restart <servicio>
```

### Acceso a Logs
```bash
# Logs de n8n
docker logs n8n

# Logs de Evolution API
docker logs evolution_api

# Logs de PostgreSQL
docker logs evolution_postgres
```

## 📚 Recursos Adicionales

- [Documentación oficial de n8n](https://docs.n8n.io/)
- [Evolution API Documentation](https://doc.evolution-api.com/)
- [Docker Compose Reference](https://docs.docker.com/compose/)

## 🛠️ Desarrollo

Este proyecto está diseñado para fines educativos. Cada workflow creado durante las clases representa un ejemplo práctico de automatización que puede ser adaptado para casos de uso reales.

---

**Creado por**: Iván Martínez  
**Institución**: CCOL  
**Nota**: Este es un proyecto educativo del curso de n8n. Los workflows y configuraciones están optimizados para aprendizaje y experimentación.
