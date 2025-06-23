# Documento de Requisitos del Sistema (DRS) - Tarea 4: Requisitos de Información

**Proyecto:** Distribuidora Leo Web
**Versión:** 1.0
**Fecha:** 22 de abril de 2025

## 1. Introducción

Esta tarea presenta los requisitos de almacenamiento y las reglas de negocio relacionadas con la información que deberá gestionar el sistema web de Distribuidora Leo. A partir de la información recolectada en tareas anteriores, se identifican las estructuras de datos necesarias, su prioridad y las restricciones para garantizar consistencia y trazabilidad.

## 2. Requisitos de Almacenamiento de Información

| **Código** | **Requisito de Información** | **Descripción**                                                                                            | **Prioridad** | **Conflictos/Revisión**        |
| ---------- | ---------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------- | ------------------------------ |
| INF-01     | Datos de productos           | Registro de nombre, categoría, precio, descripción, imagen, y cantidad disponible de cada producto.        | Alta          | Sin conflictos actuales        |
| INF-02     | Datos de clientes            | Registro de nombre completo, teléfono, dirección, correo electrónico e historial de compras.               | Alta          | Sin conflictos actuales        |
| INF-03     | Datos de pedidos             | Cada pedido debe incluir fecha, cliente asociado, productos solicitados, cantidad, estado y observaciones. | Alta          | Sin conflictos actuales        |
| INF-04     | Historial de interacciones   | Seguimiento de pedidos, fechas, cambios de estado, observaciones.                                          | Media         | A considerar en el backend     |
| INF-05     | Datos de usuarios internos   | Registro de asesoras y administrador con sus roles, accesos y actividad.                                   | Alta          | Validado en la reunión inicial |

## 3. Requisitos de Restricciones de Información y Reglas de Negocio

| **Código** | **Restricción/Regla de Negocio** | **Descripción**                                                              | **Prioridad** | **Conflictos/Revisión**  |
| ---------- | -------------------------------- | ---------------------------------------------------------------------------- | ------------- | ------------------------ |
| REG-01     | Unicidad de producto             | Cada producto debe tener un identificador único.                             | Alta          | Sin conflictos actuales  |
| REG-02     | Stock no negativo                | El sistema no debe permitir pedidos con productos fuera de stock.            | Alta          | Confirmado en la reunión |
| REG-03     | Validación de datos              | Todos los campos del cliente deben ser obligatorios al momento del registro. | Alta          | Sin conflictos actuales  |
| REG-04     | Asociación cliente-pedido        | Todo pedido debe estar vinculado a un cliente registrado.                    | Alta          | Sin conflictos actuales  |
| REG-05     | Privacidad de datos              | Acceso restringido a información personal solo a personal autorizado.        | Alta          | Alineado con OBJ-07      |

## 4. Técnica Aplicada

Se utilizaron las plantillas de requisitos de almacenamiento y restricciones de información (sección 5.2 de la metodología) para identificar y detallar los datos relevantes y las reglas de negocio, asegurando alineación con los objetivos y necesidades del cliente.

## 5. Próximos pasos

* Documentar los requisitos funcionales y no funcionales (Tarea 5).
* Iniciar el diseño del modelo de base de datos e interfaces de usuario.

**Autor:** Henry David Suárez Serrano
**Revisado por:** Equipo Distribuidora Leo
