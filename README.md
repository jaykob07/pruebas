# PRUEBA TÉCNICA DESARROLLO

## DESCRIPCIÓN DEL PROBLEMA

La empresa Celsia Internet S.A.S. requiere implementar una solución para su proceso de venta que permita la captura de información de los clientes y la contratación de uno o varios servicios del portafolio de internet.

El ejercicio consiste en implementar un backend y fontend con desplegados en contenedores, para el registro y consulta de la información de los servicios contratados por los clientes, de acuerdo con el modelo de datos presentado a continuación.

## MODELO DE DATOS

Las tablas donde se almacena la información son las siguientes:

```
CREATE TABLE clientes {
  identificacion VARCHAR(20) NOT NUL PRIMARY KEY,
  tipoIdentificacion VARCHAR(20) NOT NUL PRIMARY KEY,
  nombres VARCHAR(80) NOT NULL,
  apellidos VARCHAR(80) NOT NULL,
  tipoIdentificacion VARCHAR(2) NOT NULL,
  fechaNacimiento DATE NOT NULL,
  numeroCelular VARCHAR(20) NOT NULL,
  correoElectronico VARCHAR(80) NOT NULL
};


CREATE TABLE servicios {
  identificacion VARCHAR(20) NOT NUL,
  servicio VARCHAR(250) NOT NUL,
  fechaInicio DATE NOT NULL,
  ultimaFacturacion DATE NOT NULL,
  ultimoPago INTEGER NOT NUL DEFAULT 0
}
```

Para la prueba se debe crear las tablas en el motor de base de datos de su preferencia. Sobre esta base se deben almacenar los registros de los clientes y servicios que se especifican para la prueba.

## Puntos de la prueba

1. Implemente en el lenguaje de su preferencia, una forma que permita capturar la información de los clientes.

Tener en cuenta que los controles a utilizar deben realizar las siguientes validaciones:
• No dejar datos en blanco.
• El tipo de dato, de acuerdo con la estructura en la base de datos.
• Si el registro ya existe muestre el mensaje “el registro ya existe”.

2. Implementar un formulario que permita registrar los servicios contratados de los clientes. Nota: Tener en cuenta integridad referencial.

3. Implementar un formulario para la consultar por número de identificación la información de un cliente y los servicios que tiene contratados.

TIPS:

1. Para el campo TIPOIDENTIFICACION ingresar solamente los siguientes tipos:
   CEDULA → CC
   TARJETA IDENTIDAD → TI
   CEDULA EXTRANJERIA → CE
   REGISTRO CIVIL → RC

2. Para el campo ESTADOCIVIL solo se debe permitir los siguientes tipos:
   SOLTERO → 1
   CASADO → 2
   UNION LIBRE → 3

3. Para el campo SERVICIO ingresar solamente los siguientes tipos:
   Internet 200 MB
   Internet 400 MB
   Internet 600 MB
   Directv Go
   Paramount+
   Win+
