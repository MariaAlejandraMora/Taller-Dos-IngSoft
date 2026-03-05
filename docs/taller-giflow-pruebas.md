# Documento de Pruebas

## 1. Descripcion del Sistema

## 2. Requerimientos a Evaluar
### RF1-01 Registro de Estudiante
El sistema debe permitir el registro de estudiantes cuya edad esté entre 16 y 65 años inclusive.
## 3. Tecnicas de Prueba Aplicadas
### RF1-01 Registro de Estudiante
**Analisis de valor limite (BVA)**
### Justificacion 
Se utilizo esta tecnica porque sirve para probar una entrada con un rango numerico definido, lo cual es necesario en este requerimiento porque la entrada debe estar entre un rango de edad (16-65).

## 4. Casos de Prueba Diseñados
### RF1-01 Registro de Estudiante
| Caso | Edad | Resultado |
|------|--------|----------|
| C1 | 66 | Invalido |
| C2 | 17 | Valido |
## 5. Trazabilidad

| Requerimiento | Técnica Aplicada | Casos Asociados |
|---------------|------------------|-----------------|
| RF-01 | Valor límite | C1 (Caso invalido), C2 (Caso valido) |
| RF-02 | Partición de equivalencia | Caso valido, Caso invalido  |
| RF-03 | Tabla de decisión | CP01, CP02 |

## 6. Gestion de Versiones (GitFlow)
