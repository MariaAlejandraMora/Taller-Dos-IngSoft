# Documento de Pruebas

## 1. Descripcion del Sistema

## 2. Requerimientos a Evaluar
    
### RF1-01 Registro de Estudiante
El sistema debe permitir el registro de estudiantes cuya edad esté entre 16 y 65 años inclusive.

### RF-02 Código de Estudiante
El código del estudiante 🤓 debe:
 - Tener exactamente 8 caracteres.
 - Iniciar con la letra “E”.
 - Los 7 caracteres restantes deben ser numéricos.

### RF-03 Inscripción a Evento
Un estudiante podrá inscribirse a un evento solo si:

Está registrado.
El evento tiene cupos disponibles.
No está previamente inscrito.
Si alguna condición no se cumple, el sistema no debe permitir la inscripción.

## 3. Tecnicas de Prueba Aplicadas

### RF1-01 Registro de Estudiante
**Analisis de valor limite (BVA)**
### Justificacion 
Se utilizo esta tecnica porque sirve para probar una entrada con un rango numerico definido, lo cual es necesario en este requerimiento porque la entrada debe estar entre un rango de edad (16-65).

### RF-02 Código de Estudiante
**Participación de equivalencia**
### Justificación 
Se utiliza partición de equivalencia debido a que  el requerimiento define reglas claras sobre la estructura y formato del código, lo que permite dividir las entradas en clases válidas e inválidas para verificar que el sistema solo acepte códigos con el formato correcto.
| **Criterio**                 | **Clases válidas**                                  | **Clases inválidas**                        |
|------------------------------|-----------------------------------------------------|-----------------------------------------------|
| Longitud del código          | V1: Exactamente 8 caracteres                        | I1: Menos de 8 caracteres  -  I2: Más de 8 caracteres  |
| Letra inicial                | V2: Inicia con la letra "E"                         | I3: No inicia con la letra "E"                |
| Caracteres numéricos         | V3: Los 7 caracteres restantes son numéricos        | I4: Contiene letras o símbolos en lugar de números |

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

### RF1-01 Registro de Estudiante
| Caso | Edad | Resultado |
|------|--------|----------|
| C1 | 66 | Invalido |
| C2 | 17 | Valido |

### RF-02 Código de Estudiante
| **Nombre**      | **Valores de entrada** | **Salida esperada**|
|-----------------|-------------------|-----------------|
| Código válido   | code: "E1234567"  | TRUE            |
| Código inválido | code: "E12345A7"  | FALSE           |

### RF-03 Inscripción a Evento

| Nombre | Escenario | resultado |
|------|------|------|
| CP01 | El estudiante está registrado en el sistema. El evento tiene cupos disponibles. El estudiante no está previamente inscrito. |true|
| CP02 | El estudiante NO está registrado. El evento tiene cupos disponibles. El estudiante no está previamente inscrito. |false|


## 5. Trazabilidad

| Requerimiento | Técnica Aplicada | Casos Asociados |
|---------------|------------------|-----------------|
| RF-01 | Valor límite | C1 (Caso invalido), C2 (Caso valido) |
| RF-02 | Partición de equivalencia | Caso valido, Caso invalido  |
| RF-03 | Tabla de decisión | CP01, CP02 |

## 6. Gestion de Versiones (GitFlow)
