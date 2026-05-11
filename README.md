# 📅 Sistema de Gestión y Generación Automática de Horarios

> **TFG (Trabajo Fin de Grado) - Aplicación Web FullStack para la gestión inteligente de ciclos formativos, asignaturas, profesorado y generación automática de horarios utilizando algoritmos de optimización.**

---

## 🎯 Acerca del Proyecto

Este proyecto es una **aplicación web profesional** desarrollada como Trabajo Fin de Grado, diseñada para resolver el complejo problema de la planificación académica en centros educativos. La solución automatiza la generación de horarios considerando múltiples restricciones y optimizaciones.

### El Problema que Resuelve

La gestión manual de horarios en centros educativos es:
- ⏰ **Consumidora de tiempo**: Tarea que requiere horas de trabajo manual
- 🤔 **Propensa a errores**: Conflictos de profesores, solapamientos, incompatibilidades
- 📊 **Difícil de optimizar**: Balancear carga docente, preferencias y disponibilidad
- 📄 **Complicada de mantener**: Cambios y ajustes posteriores son tediosos

### La Solución

Una plataforma web completa que:
- ✅ Automatiza la generación de horarios con **algoritmos de optimización**
- 🔄 Reduce el tiempo de planificación de horas a minutos
- 🎯 Elimina conflictos automáticamente
- 📱 Proporciona una interfaz intuitiva y moderna
- 👥 Permite consultar horarios personalizados por profesor, ciclo o departamento
- 📥 Exporta horarios a PDF de forma profesional
- 🔐 Controla acceso mediante autenticación robusta

---

## ✨ Lo que Puedes Hacer

- 📋 **Gestionar toda la información**: Ciclos, asignaturas, profesores y horarios en un solo lugar
- 🤖 **Generar horarios automáticamente**: En segundos, sin conflictos de profesores
- 👥 **Cada profesor consulta su horario**: Interfaz personalizada y amigable
- 📄 **Exportar a PDF**: Horarios listos para imprimir o compartir
- 🔐 **Acceso seguro**: Solo usuarios autorizados ven información confidencial
- 📊 **Ver toda la historia**: Registro completo de quién hizo qué y cuándo

---

## 🏗️ Cómo Funciona

```
El usuario entra → Sistema verifica su identidad → Accede a su área
                           ↓
                    Gestiona sus datos
                  (ciclos, asignaturas, etc.)
                           ↓
                    Pide generar horarios
                           ↓
              Sistema automático calcula la mejor
              distribución sin conflictos (segundos)
                           ↓
                    Horario disponible
                  (pantalla + PDF listo)
```

---

## 🛠️ Tecnologías Utilizadas

**Interfaz moderna**: React (framework de Facebook)  
**Servidor**: PHP 8 (lenguaje web profesional)  
**Base de datos**: MySQL (la más usada en empresas)  
**Motor inteligente**: Algoritmo avanzado de optimización (Google OR-Tools)  
**Despliegue**: Google Cloud Platform (infraestructura profesional)

---

## 📸 Interfaz en Acción

### 1. Inicio de Sesión
Pantalla de autenticación segura para acceder a la aplicación.

![Inicio de Sesión](img/iniciosesion.png)

---

### 2. Pantalla Principal
Panel de control intuitivo con acceso a todas las funciones de la aplicación. Interfaz limpia y moderna preparada para gestionar los datos.

![Pantalla Principal](img/pantallaprincipal.png)

---

### 3. Registrar Nuevo Ciclo
Gestión completa de ciclos formativos y asignaturas. Visualiza la tabla con todos los ciclos disponibles y sus asignaturas, y los formularios para registrar nuevos ciclos con sus datos.

![Registrar Nuevo Ciclo](img/registrarnuevociclo.png)

---

### 4. Generación Exitosa
Confirmación de la generación automática exitosa de horarios. Mensaje de éxito tras ejecutar el algoritmo de optimización.

![Generación Exitosa](img/genereacionexitosa.png)

---

### 5. Vista Dividida
Visualización avanzada utilizando DockView para una experiencia dividida. Panel superior con el framework de dockview y panel inferior mostrando el horario generado de forma clara y organizada.

![Vista Dividida](img/vistadividida.png)
- Crear ciclos, asignaturas, profesores
- Interfaz fácil de usar
- Sin necesidad de conocimientos técnicos
```

---

## 🚀 Demostración en Vivo

Este proyecto fue desarrollado y desplegado en Google Cloud Platform con acceso público vía SSH. La interfaz es completamente funcional con:

- ✅ Autenticación de usuarios con JWT
- ✅ Gestión de ciclos, asignaturas y profesores
- ✅ Generación automática de horarios con CP-SAT
- ✅ Exportación a PDF
- ✅ Historial de operaciones con auditoría

### Stack Implementado
- **Frontend**: React 19 con interfaz de paneles (Dockview)
- **Backend**: PHP 8.x con API REST
- **Motor**: Python OR-Tools CP-SAT
- **Base de Datos**: MySQL/MariaDB

---

---

## 🔌 API REST - Endpoints Principales

### Autenticación
```
POST   /api/login.php          # Login con usuario/contraseña
POST   /api/logout.php         # Cierre de sesión
POST   /api/refresh.php        # Renovar token JWT
```

### Gestión de Ciclos
```
GET    /api/get_ciclos.php               # Listar ciclos
GET    /api/get_ciclos_detalle.php       # Ciclo con detalle de asignaturas
POST   /api/add_ciclo.php                # Crear ciclo
PUT    /api/update_ciclo.php             # Actualizar ciclo
DELETE /api/delete_horario.php           # Eliminar horario de ciclo
```

### Gestión de Asignaturas
```
GET    /api/get_asignaturas_detalle.php  # Listar con profesores
POST   /api/add_asignatura.php           # Crear asignatura
PUT    /api/update_asignatura_profesores.php  # Asignar profesores
DELETE /api/delete_asignatura.php        # Eliminar asignatura
```

### Gestión de Profesores
```
GET    /api/get_profesores.php           # Listar profesores
GET    /api/get_profesores_detalle.php   # Con asignaturas asociadas
POST   /api/add_profesor.php             # Crear profesor
PUT    /api/update_profesor_asignaturas.php  # Asignar asignaturas
DELETE /api/delete_profesor.php          # Eliminar profesor
```

### Generación de Horarios
```
POST   /api/preparar_generacion.php      # Preparar generación
POST   /api/generar_horario.php          # Ejecutar solver CP-SAT
GET    /api/get_horario.php              # Obtener horario por ciclo
GET    /api/get_horario_profesor.php     # Obtener horario por profesor
```

### Otros
```
GET    /api/get_logs.php         # Historial de operaciones
GET    /api/get_usuarios.php     # Gestión de usuarios
```

---

## 🧠 Motor de Optimización: Cómo Funciona

### El Problema (Problema de Programación)

Dado:
- **N** ciclos formativos
- **M** asignaturas
- **P** profesores
- **T** slots de tiempo (franjas horarias)
- **R** aulas/recursos

Encontrar: Una asignación de (ciclo, asignatura, profesor, aula, tiempo) que:

### Las Restricciones

1. **No hay solapamientos**: Cada profesor solo puede estar en una clase a la vez
2. **Ciclos completos**: Todas las asignaturas de un ciclo deben tener horario
3. **Disponibilidad**: Se respeta la disponibilidad de profesores
4. **Carga equitativa**: Se distribuye la carga docente entre profesores
5. **Recreos**: Se insertan automáticamente en franjas definidas

### La Solución

Usamos **Google OR-Tools CP-SAT**, un solver de programación por restricciones que:
- ✅ Es rápido (resuelve en segundos incluso con 100+ variables)
- ✅ Es robusto (maneja restricciones complejas)
- ✅ Es portable (funciona en cualquier plataforma)
- ✅ Proporciona diagnósticos claros cuando no hay solución

**Proceso:**
```
1. Lectura de datos desde BD
2. Construcción del modelo de restricciones (Python)
3. Ejecución del solver CP-SAT
4. Análisis de resultados
5. Inserción de recreos automáticos
6. Almacenamiento en BD
7. Retorno a frontend con detalles de éxito/error
```

---

## 🔒 Seguridad

### Autenticación y Autorización
- **JWT**: Tokens firmados con expiración configurable
- **Sesiones en BD**: Revocación inmediata de tokens
- **Validación de User-Agent**: Anti-robo de tokens
- **Roles granulares**: Superadmin vs usuario normal
- **Hashing de contraseñas**: bcrypt con salt

### Protección
- **CORS**: Configurado por origen
- **CSRF**: Validación de tokens para operaciones mutables
- **SQL Injection**: Prepared statements (PDO)
- **XSS**: Escapado de salida en templates
- **Rate limiting**: Posibilidad de implementar fácilmente

---

## 🐛 Troubleshooting y Diagnóstico

### Error: "Python no encontrado"
```
Solución: Verificar que Python 3.8+ está en PATH
Verificar: python --version
Instalar OR-Tools: pip install ortools
```

### Error: "No se puede conectar a base de datos"
```
Solución: Revisar credenciales en config/env.php
Verificar: MySQL está ejecutándose
Comprobar: Usuario y contraseña coinciden
```

### Error: "Solver no encuentra solución"
```
Información técnica en el modal de generación
Posibles causas:
- Demasiados profesores para pocas asignaturas
- Profesores con disponibilidad muy limitada
- Restricciones conflictivas
Solución: Ajustar datos y reintentar
```

---

## 📊 Estadísticas del Proyecto

| Métrica | Valor |
|---------|-------|
| **Líneas de código** | ~5,000+ |
| **Endpoints API** | 30+ |
| **Componentes React** | 15+ |
| **Tablas BD** | 10+ |
| **Lenguajes** | PHP, Python, JavaScript, SQL |
| **Horas de desarrollo** | 200+ |

---

---

## 👨‍💼 Autor

**Desarrollador**: Alfonso Carrasco Salgueiro  
**Institución**: MEDAC-DAVANTE  
**Año**: 2026  
**Contacto**: alfonso.salgueiro.carrasco@gmail.com

---

## 🎓 Este es un Proyecto Académico

Desarrollado como **Trabajo Fin de Grado (TFG)** demostrando:
- ✅ Análisis y diseño de sistemas complejos
- ✅ Arquitectura fullstack moderna
- ✅ Integración de algoritmos de optimización
- ✅ Desarrollo web profesional
- ✅ Seguridad en aplicaciones web
- ✅ Buenas prácticas de programación

---


**⭐ Si este proyecto te resulta útil, considera darle una estrella en GitHub**
