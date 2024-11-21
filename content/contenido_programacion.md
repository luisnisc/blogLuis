+++
date = '2024-11-20T16:46:48+01:00'
draft = false
title = 'Contenido Programación'
weight = 4
+++

# JavaScript

## **Introducción**

### **¿Qué es JavaScript?**

JavaScript es un lenguaje de programación interpretado, orientado a objetos y débilmente tipado. Se utiliza principalmente para añadir interactividad y dinamismo a las páginas web, permitiendo a los desarrolladores crear experiencias más enriquecedoras para los usuarios.

### **¿Por qué Aprender JavaScript?**

- **Versatilidad**: Se puede usar tanto en el frontend como en el backend.
- **Comunidad Amplia**: Gran cantidad de recursos y soporte.
- **Demanda Laboral**: Muchas compañías buscan desarrolladores con conocimientos en JavaScript.

## **Fundamentos de JavaScript**

### **Sintaxis Básica**

```javascript
// Esto es un comentario
let mensaje = '¡Hola, mundo!';
console.log(mensaje);
```

### **Variables y Tipos de Datos**
- **Variables**: Se pueden declarar con `var`, `let` o `const`.
- **Tipos de Datos**: Números, cadenas, booleanos, objetos, funciones, etc.

```javascript
let edad = 25;              // Número
const nombre = `Ana`;       // Cadena
var esEstudiante = true;    // Booleano
```

### **Operadores**
- **Aritméticos**: `+`, `-`, `*`, `/`, `%`.
- **Asignación**: `=`, `+=`, `-=`, `*=`, `/=`, `%=`.
- **Comparación**: `==`, `===`, `!=`, `>`, `<`, `>=`, `<=`.
- **Lógicos**: `&&`, `||`, `!`.

```javascript
let resultado = (10 + 5) * 2;
```

### **Estructuras de Control (if, switch, bucles)**

- **Condicional if**
```javascript
if (edad>= 18){
    console.log('Eres mayor de edad');
} else {
    console.log('Eres menor de edad');
}
```

- **Switch**
```javascript
let diaSemana = 3;
switch (diaSemana){
    case 1:
        console.log('Lunes');
        break;
    case 2:
        console.log('Martes');
        break;
    default:
        console.log('Otro día');
}
```

- **Bucles(for, while, do-while)**
```javascript
for (let i = 0; i < 5; i++){
    console.log(i);
}
```
```javascript
let i = 0;
while (i < 5){
    console.log(i);
    i++;
}
```
```javascript
let i = 0;
do {
    console.log(i);
    i++;
} while (i < 5);
```

### **Funciones**
- **Declaración y Uso de Funciones**
```javascript
function suma(a, b){
    return a + b;
}

let total = sumar(5,3);
```

- **Funciones Anónimas**
```javascript
let multiplicar = function(a, b){
    return a * b;
}
```

- **Funciones Flecha**
```javascript
let dividir = (a, b) => a / b;
```

### Parámetros y Argumentos

```javascript

function saludar(nombre){
    console.log(`¡Hola, ${nombre}!`);
}

saludar('Ana');
```

### **Arrays y Objetos**

#### **Creación y Manipulación de Objetos**

```javascript

let persona = {
    nombre: 'Ana',
    edad: 25,
    saludar: function(){
        console.log(`¡Hola, soy ${this.nombre}!`);
    }
}
persona.saludar();
```

#### **Arrays y Métodos de Arrays**

```javascript
let frutas = ['Manzana', 'Banana', 'Cereza'];

frutas.push('Naranja');        // Añade al final
frutas.unshift('Fresa');       // Añade al inicio
frutas.pop();                  // Elimina último elemento

console.log(frutas);  // ['Fresa', 'Manzana', 'Banana', 'Cereza']
```

#### **Iteración sobre Arrays y Objetos**

- **ForEach**
```javascript
frutas.forEach(function(fruta){
    console.log(fruta);
});
```

- **For-In**
```javascript
for (let propiedad in persona){
    console.log(`${propiedad}: ${persona[propiedad]}`);
}
```

- **Map**
```javascript
let numeros = [1, 2, 3, 4, 5];
let dobles = numeros.map(function(numero){
    return numero * 2;
});
console.log(dobles);  // [2, 4, 6, 8, 10]
```

### **Manipulación del DOM**
#### **Selección de Elementos**
```javascript
let titulo = document.getElementById('titulo');
let parrafos = document.getElementsByClassName('parrafo');  
let botones = document.querySelectorAll('button');          
```

#### **Eventos y Manejadores de Eventos**
```javascript
let boton = document.getElementById('miBoton');
boton.addEventListener('click', function() {
  alert('¡Botón presionado!');
});
```

#### **Modificación de Contenido y Estilo del DOM**
```javascript
titulo.textContent = 'Nuevo Título';
titulo.style.color = 'red';
```

### **Asincronía y Promesas**

#### **Callbacks**
```javascript
function descargarArchivo(url, callback) {
  setTimeout(function() {
    console.log('Archivo descargado de ' + url);
    callback();
  }, 2000);
}

descargarArchivo('http://ejemplo.com/archivo', function() {
  console.log('Descarga completa');
});
```

#### **Promesas**
```javascript
function promesaEjemplo() {
  return new Promise(function(resolve, reject) {
    let exito = true;
    if (exito) {
      resolve('Operación exitosa');
    } else {
      reject('Error en la operación');
    }
  });
}

promesaEjemplo()
  .then(function(mensaje) {
    console.log(mensaje);
  })
  .catch(function(error) {
    console.log(error);
  });
```

#### **Async/Await**
```javascript
async function obtenerUsuario() {
  try {
    let respuesta = await fetch('https://api.ejemplo.com/usuario');
    let datos = await respuesta.json();
    console.log(datos);
  } catch (error) {
    console.error('Error:', error);
  }
}

obtenerUsuario();
```

### **APIs del Navegador**

#### **Fetch API**
```javascript
fetch('https://api.ejemplo.com/datos')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error:', error));
```

#### **LocalStorage y SessionStorage**
```javascript
// LocalStorage
localStorage.setItem('usuario', 'Ana');
let usuario = localStorage.getItem('usuario');

// SessionStorage
sessionStorage.setItem('token', 'ABC123');
let token = sessionStorage.getItem('token');
```




