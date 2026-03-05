# Documento de Pruebas

## 1. Descripcion del Sistema

## 2. Requerimientos a Evaluar

### RF-02 Código de Estudiante
El código del estudiante 🤓 debe:
 - Tener exactamente 8 caracteres.
 - Iniciar con la letra “E”.
 - Los 7 caracteres restantes deben ser numéricos.
      
## 3. Tecnicas de Prueba Aplicadas

### RF-02 Código de Estudiante
**Participación de equivalencia**
### Justificación 
Se utiliza partición de equivalencia debido a que  el requerimiento define reglas claras sobre la estructura y formato del código, lo que permite dividir las entradas en clases válidas e inválidas para verificar que el sistema solo acepte códigos con el formato correcto.
| Criterio                     | Clases válidas (V)                                  | Clases inválidas (I)                         |
|------------------------------|-----------------------------------------------------|-----------------------------------------------|
| Longitud del código          | V1: Exactamente 8 caracteres                        | I1: Menos de 8 caracteres  -  I2: Más de 8 caracteres  |
| Letra inicial                | V2: Inicia con la letra "E"                         | I3: No inicia con la letra "E"                |
| Caracteres numéricos         | V3: Los 7 caracteres restantes son numéricos        | I4: Contiene letras o símbolos en lugar de números |


## 4. Casos de Prueba Diseñados
### RF-02 Código de Estudiante


## 5. Trazabilidad

## 6. Gestion de Versiones (GitFlow)
