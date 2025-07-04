# Estadística y Probabilidades  
**Trabajo Práctico Nro 4**  
**Formularios**

## Objetivo
Integrar conocimientos de programación web con conceptos estadísticos a través de la recolección y registro de datos reales mediante formularios y APIs.

---

## Instrucciones

Desarrollar una página HTML con un formulario que permita ingresar datos de alumnos.  
Debe contener los siguientes campos:

- **Nombre** (campo de texto)  
- **Apellido** (campo de texto)  
- **DNI** (campo numérico o texto)  
- **Fecha de nacimiento** (selector de fecha)  
- **Sexo** (desplegable con opciones H y M)  
- **Edad** (campo numérico)  
- **ID de curso** (campo numérico)  
- **ID de nivel** (campo numérico)

Al hacer clic en "Enviar", el formulario debe capturar los datos y enviarlos al endpoint que se describe a continuación:

- El envío debe realizarse usando JavaScript (`fetch()`) con el cuerpo en formato JSON.  
- Mostrar al usuario si la operación fue exitosa o si hubo errores (por ejemplo:  
  `"Alumno registrado correctamente"` o `"El DNI ya existe"`).

---

## Consumo de API

La API recibirá los datos que el formulario envíe por **POST** en la siguiente URL:  
`https://apidemo.geoeducacion.com.ar/api/testing/formulario/1`

- Enviar los datos en formato **JSON** usando `Content-Type: application/json`.

### Ejemplo del cuerpo:

```json
{
  "Nombre": "Sofía",
  "Apellido": "Pérez",
  "DNI": "45678912",
  "Fecha_de_nacimiento": "2006-05-15",
  "Sexo": "F",
  "Edad": 18,
  "ID_Curso": 4,
  "ID_Nivel": 2
}
```

### Respuesta esperada en caso de éxito:

```json
{
  "success": true,
  "message": "Alumno registrado correctamente"
}
```

### Respuesta esperada en caso de error:

```json
{
  "success": false,
  "errors": {
    "DNI": [
      "El campo DNI es obligatorio."
    ]
  }
}
```

---

## Validaciones aplicadas

- **Nombre**: obligatorio, máximo 255 caracteres  
- **Apellido**: obligatorio, máximo 255 caracteres  
- **DNI**: obligatorio, máximo 15 caracteres, no debe repetirse  
- **Fecha_de_nacimiento**: obligatorio, formato `YYYY-MM-DD`  
- **Sexo**: obligatorio, solo se acepta `"M"` o `"F"`  
- **Edad**: obligatorio, valor entre 1 y 120  
- **ID_Curso**: obligatorio  
- **ID_Nivel**: obligatorio, valores entre 1 y 3  

---

## Opcionales

### OPCIONAL 1:
Mostrar una lista de los estudiantes registrados, en donde se refleje la inserción hecha. Para ello podrá usar los servicios empleados con trabajos anteriores.

### OPCIONAL 2:
Verificar en prácticos anteriores cómo se alteran los estadísticos calculados luego de la inserción de nuevos alumnos.
# Estadística y Probabilidades  
**Trabajo Práctico Nro 4**  
**Formularios**

## Objetivo
Integrar conocimientos de programación web con conceptos estadísticos a través de la recolección y registro de datos reales mediante formularios y APIs.

---

## Instrucciones

Desarrollar una página HTML con un formulario que permita ingresar datos de alumnos.  
Debe contener los siguientes campos:

- **Nombre** (campo de texto)  
- **Apellido** (campo de texto)  
- **DNI** (campo numérico o texto)  
- **Fecha de nacimiento** (selector de fecha)  
- **Sexo** (desplegable con opciones H y M)  
- **Edad** (campo numérico)  
- **ID de curso** (campo numérico)  
- **ID de nivel** (campo numérico)

Al hacer clic en "Enviar", el formulario debe capturar los datos y enviarlos al endpoint que se describe a continuación:

- El envío debe realizarse usando JavaScript (`fetch()`) con el cuerpo en formato JSON.  
- Mostrar al usuario si la operación fue exitosa o si hubo errores (por ejemplo:  
  `"Alumno registrado correctamente"` o `"El DNI ya existe"`).

---

## Consumo de API

La API recibirá los datos que el formulario envíe por **POST** en la siguiente URL:  
`https://apidemo.geoeducacion.com.ar/api/testing/formulario/1`

- Enviar los datos en formato **JSON** usando `Content-Type: application/json`.

### Ejemplo del cuerpo:

```json
{
  "Nombre": "Sofía",
  "Apellido": "Pérez",
  "DNI": "45678912",
  "Fecha_de_nacimiento": "2006-05-15",
  "Sexo": "F",
  "Edad": 18,
  "ID_Curso": 4,
  "ID_Nivel": 2
}
```

### Respuesta esperada en caso de éxito:

```json
{
  "success": true,
  "message": "Alumno registrado correctamente"
}
```

### Respuesta esperada en caso de error:

```json
{
  "success": false,
  "errors": {
    "DNI": [
      "El campo DNI es obligatorio."
    ]
  }
}
```

---

## Validaciones aplicadas

- **Nombre**: obligatorio, máximo 255 caracteres  
- **Apellido**: obligatorio, máximo 255 caracteres  
- **DNI**: obligatorio, máximo 15 caracteres, no debe repetirse  
- **Fecha_de_nacimiento**: obligatorio, formato `YYYY-MM-DD`  
- **Sexo**: obligatorio, solo se acepta `"M"` o `"F"`  
- **Edad**: obligatorio, valor entre 1 y 120  
- **ID_Curso**: obligatorio  
- **ID_Nivel**: obligatorio, valores entre 1 y 3  

---

## Opcionales

### OPCIONAL 1:
Mostrar una lista de los estudiantes registrados, en donde se refleje la inserción hecha. Para ello podrá usar los servicios empleados con trabajos anteriores.

### OPCIONAL 2:
Verificar en prácticos anteriores cómo se alteran los estadísticos calculados luego de la inserción de nuevos alumnos.
