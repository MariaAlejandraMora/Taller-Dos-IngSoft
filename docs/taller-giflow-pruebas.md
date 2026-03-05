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



## 5. Trazabilidad

## 6. Gestion de Versiones (GitFlow)
