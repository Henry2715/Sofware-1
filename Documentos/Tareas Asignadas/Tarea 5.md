# Documento de Requisitos del Sistema (DRS) - Tarea 5: Requisitos Funcionales

**Proyecto:** Distribuidora Leo Web
**Versión:** 1.0
**Fecha:** 26 de abril de 2025

## 1. Introducción

Esta tarea presenta los requisitos funcionales del sistema web propuesto para Distribuidora Leo. Se identifican los actores principales y se describen los casos de uso clave del sistema, asegurando trazabilidad con los objetivos definidos en la Tarea 3 y los requisitos de información de la Tarea 4. El enfoque sigue las plantillas recomendadas por la metodología de Durán & Bernárdez (2002).

## 2. Identificación de Actores

| Actor             | Descripción                                                                 |
| ----------------- | --------------------------------------------------------------------------- |
| **Cliente**       | Usuario final que navega el catálogo, registra sus datos y realiza pedidos. |
| **Asesora**       | Usuario interno que gestiona pedidos y contacto con clientes.               |
| **Administrador** | Responsable de administrar productos, clientes y reportes.                  |
| **Sistema Web**   | Plataforma que gestiona las operaciones del negocio.                        |

## 3. Requisitos Funcionales (Casos de Uso)

### 3.1. Caso de Uso: Registrar Cliente

| Elemento            | Descripción                                                                                                                                         |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nombre**          | Registrar Cliente                                                                                                                                   |
| **Actor principal** | Cliente                                                                                                                                             |
| **Descripción**     | Permite a un cliente registrarse con sus datos para crear un perfil.                                                                                |
| **Precondición**    | El cliente accede por primera vez al sistema.                                                                                                       |
| **Flujo principal** | 1. Ingresa a la opción "Registrarse".<br>2. Completa formulario con sus datos.<br>3. Envía el formulario.<br>4. El sistema almacena la información. |
| **Alternativas**    | Si ya está registrado, puede iniciar sesión.                                                                                                        |
| **Excepciones**     | Datos incompletos o inválidos (se notifican con un mensaje).                                                                                        |
| **Postcondición**   | El cliente queda registrado en la base de datos.                                                                                                    |

### 3.2. Caso de Uso: Visualizar Catálogo

| Elemento            | Descripción                                                                                                             |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| **Nombre**          | Visualizar Catálogo                                                                                                     |
| **Actor principal** | Cliente                                                                                                                 |
| **Descripción**     | Permite al cliente ver los productos ofrecidos por la empresa.                                                          |
| **Precondición**    | El cliente accede al sistema.                                                                                           |
| **Flujo principal** | 1. Ingresa al módulo de catálogo.<br>2. Explora productos por categoría o nombre.<br>3. Consulta detalles del producto. |
| **Alternativas**    | Utiliza buscador para filtrar productos.                                                                                |
| **Excepciones**     | El catálogo no tiene productos disponibles (mensaje informativo).                                                       |
| **Postcondición**   | El cliente visualiza los productos.                                                                                     |

### 3.3. Caso de Uso: Registrar Pedido

| Elemento            | Descripción                                                                                                                   |
| ------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Nombre**          | Registrar Pedido                                                                                                              |
| **Actor principal** | Cliente                                                                                                                       |
| **Descripción**     | El cliente selecciona productos y genera un pedido.                                                                           |
| **Precondición**    | El cliente ha iniciado sesión o registrado sus datos.                                                                         |
| **Flujo principal** | 1. Elige productos desde el catálogo.<br>2. Los añade al carrito.<br>3. Confirma pedido.<br>4. El sistema almacena los datos. |
| **Alternativas**    | El cliente elimina o cambia productos del carrito.                                                                            |
| **Excepciones**     | El producto no tiene stock suficiente (mensaje de error).                                                                     |
| **Postcondición**   | El pedido queda registrado y notificado a la asesora.                                                                         |

### 3.4. Caso de Uso: Administrar Productos

| Elemento            | Descripción                                                                                |
| ------------------- | ------------------------------------------------------------------------------------------ |
| **Nombre**          | Administrar Productos                                                                      |
| **Actor principal** | Administrador                                                                              |
| **Descripción**     | Gestiona el alta, edición y eliminación de productos en el catálogo.                       |
| **Precondición**    | El administrador ha iniciado sesión.                                                       |
| **Flujo principal** | 1. Accede a módulo de productos.<br>2. Añade, edita o elimina ítems.<br>3. Guarda cambios. |
| **Alternativas**    | Cancelación de operación antes de guardar.                                                 |
| **Excepciones**     | Errores de validación (datos inválidos).                                                   |
| **Postcondición**   | El catálogo se actualiza correctamente.                                                    |

## 4. Requisitos Funcionales en Lenguaje Natural (Complementarios)

* El sistema debe permitir buscar productos por nombre o categoría.
* Debe existir una sección para contacto por WhatsApp directo.
* El sistema debe permitir al administrador consultar historial de pedidos y clientes.
* Las asesoras deben poder ver pedidos asignados y actualizarlos como "en proceso" o "despachado".

## 5. Revisión de Conflictos

Durante el análisis de estos requisitos no se detectaron conflictos entre actores. Las decisiones clave como mantener el contacto por WhatsApp y simplificar el formulario de registro fueron consensuadas en la Tarea 2.

## 6. Trazabilidad entre Objetivos y Requisitos Funcionales

| Objetivo                                 | Requisito Funcional Relacionado                          |
| ---------------------------------------- | -------------------------------------------------------- |
| OBJ-01: Digitalizar el proceso de ventas | Registrar Cliente, Registrar Pedido, Visualizar Catálogo |
| OBJ-02: Mejorar gestión de inventario    | Administrar Productos                                    |
| OBJ-03: Agilizar atención al cliente     | Registro simple, contacto WhatsApp, historial visible    |
| OBJ-05: Mejorar trazabilidad de pedidos  | Consultar historial, seguimiento de estado               |

## 7. Técnica Aplicada

Se utilizaron las plantillas de requisitos funcionales (sección 5.4) y de actores (sección 5.3) de la metodología de Durán & Bernárdez (2002). Se revisaron los flujos y condiciones de cada caso de uso para asegurar consistencia con los objetivos, conflictos y requisitos de información definidos en tareas anteriores.

Se utilizaron las plantillas de requisitos de almacenamiento y restricciones de información (sección 5.2 de la metodología) para identificar y detallar los datos relevantes y las reglas de negocio, asegurando alineación con los objetivos y necesidades del cliente.

## 8. Próximos pasos

* Validar estos requisitos con la administradora y asesoras.
* Documentar requisitos no funcionales (Tarea 6).

**Autor:** Henry David Suárez Serrano
**Revisado por:** Equipo Distribuidora Leo
