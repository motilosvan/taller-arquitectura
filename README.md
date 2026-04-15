# 🎟️ EventFlow - Sistema de Venta de Entradas

EventFlow es una aplicación web diseñada para la gestión y compra de entradas a eventos. Este proyecto fue desarrollado como parte de un taller de Arquitectura de Software, aplicando conceptos como microservicios, atributos de calidad, DevOps, y evaluación de usabilidad.

---

## 🚀 Tecnologías utilizadas

- HTML, CSS y JavaScript
- GitHub (Control de versiones)
- GitHub Actions (CI/CD)
- Terraform (Infraestructura como Código)
- SonarCloud (Análisis de deuda técnica)
- Trello (Gestión ágil)
- Miro (Modelado y arquitectura)
- Figma (Diseño UX/UI)

---

## 📌 Funcionalidades principales

- Visualización de eventos disponibles
- Compra simulada de entradas
- Interfaz básica de usuario
- Simulación de procesos de pago

---

## 🧠 Arquitectura del sistema

### 🔹 Monolito en capas
El sistema inicialmente se diseñó como una arquitectura monolítica con tres capas:

- Presentación (UI)
- Lógica de negocio
- Acceso a datos

**Limitación:** No permite escalar componentes de manera independiente.

---

### 🔹 Microservicios
Se rediseñó el sistema usando microservicios:

- Servicio de Usuarios
- Servicio de Eventos
- Servicio de Pedidos
- Servicio de Pagos

**Ventajas:**
- Escalabilidad horizontal
- Mantenibilidad
- Despliegue independiente

---

### 🔹 Arquitectura orientada a eventos
Los servicios se comunican mediante eventos.

Ejemplo:
- El servicio de pagos emite el evento `PagoAprobado`
- El servicio de pedidos reacciona a este evento

---

## 📊 Atributos de calidad (NFR)

- Escalabilidad: Soporte de miles de usuarios concurrentes
- Rendimiento: Respuestas rápidas (<2s)
- Seguridad: Protección de datos de pago
- Disponibilidad: Alta disponibilidad del sistema
- Modificabilidad: Facilidad de cambios

---

## 👥 Stakeholders

- Usuario: Facilidad de uso
- Finanzas: Seguridad en pagos
- Desarrolladores: Mantenibilidad
- Administradores: Control del sistema

---

## 🔄 DevOps y CI/CD

Se implementó un pipeline de integración continua con GitHub Actions:

1. Construcción del proyecto
2. Ejecución de pruebas simuladas
3. Validación automática

Esto permite procesos automatizados, repetitivos y confiables.

---

## ☁️ Infraestructura como Código (IaC)

Se utilizó Terraform para definir:

- Red virtual
- Reglas de firewall
- Servidor web

Esto permite gestionar infraestructura de forma automatizada y versionada.

---

## 🧪 Evaluación UX (Heurísticas de Nielsen)

Se identificaron problemas de usabilidad como:

- Falta de feedback al usuario
- Inconsistencia en botones
- Errores sin mensajes claros
- Falta de validaciones

Estas mejoras permiten optimizar la experiencia del usuario.

---

## 🧩 Metodologías aplicadas

### 🔹 ATAM
Evaluación de atributos de calidad y trade-offs.

### 🔹 SAAM
Análisis de modificabilidad ante cambios.

### 🔹 Heurísticas de Nielsen
Evaluación de usabilidad de la interfaz.

---

## ⚠️ Deuda técnica

El sistema incluye código con "malos olores":

- CSS mezclado con HTML
- JavaScript en línea

Esto fue intencional para análisis en SonarCloud.

---

## 📁 Estructura del proyecto
├── index.html
├── main.tf
└── .github/
└── workflows/
└── ci.yml
