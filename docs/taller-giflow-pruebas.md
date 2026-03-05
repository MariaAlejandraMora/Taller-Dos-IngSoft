# Documento de Pruebas

## 1. Descripcion del Sistema

## 2. Requerimientos a Evaluar
### RF-03 Inscripción a Evento
Un estudiante podrá inscribirse a un evento solo si:

Está registrado.
El evento tiene cupos disponibles.
No está previamente inscrito.
Si alguna condición no se cumple, el sistema no debe permitir la inscripción.


## 3. Tecnicas de Prueba Aplicadas
### RF-03 Inscripción a Evento
**Tabla de Decisión**

### Justificación

La tabla de decisión es adecuada porque el requerimiento depende de varias condiciones lógicas que deben evaluarse en conjunto.  
Esta técnica permite analizar todas las combinaciones posibles de condiciones y verificar el resultado esperado para cada una.

| ¿El estudiante está registrado? | ¿El evento tiene cupos disponibles? | ¿El estudiante ya está inscrito? | ¿Se permite la inscripción? |
|----------------------------------|--------------------------------------|----------------------------------|------------------------------|
| Sí                               | Sí                                   | No                               | Sí                           |
| No                               | Sí                                   | No                               | No                           |

## 4. Casos de Prueba Diseñados
### RF-03 Inscripción a Evento

| Nombre | Escenario | resultado |
|------|------|------|
| CP01 | El estudiante está registrado en el sistema. El evento tiene cupos disponibles. El estudiante no está previamente inscrito. |true|
| CP02 | El estudiante NO está registrado. El evento tiene cupos disponibles. El estudiante no está previamente inscrito. |false|

## 5. Trazabilidad

## 6. Gestion de Versiones (GitFlow)
