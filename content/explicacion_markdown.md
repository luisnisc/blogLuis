+++
date = '2024-11-20T16:46:47+01:00'
draft = false
title = 'Explicación de Markdown'
weight = 4
+++

# Guía Completa de Markdown

Mark down es un **lenguaje de marcado ligero** que permite formatear texto de manera sencilla y legible. Es ampliamente utilizado para crear contenido en la web, incluyendo blogs, documentación, y más.

## Encabezados

Los encabezados permiten estructurar el contenido jeráquicamente. Se utilizan mediante el símbolo `#` seguido de un espacio y el texto del encabezado.

```markdown
# Encabezado 1
## Encabezado 2
### Encabezado 3
#### Encabezado 4
##### Encabezado 5
###### Encabezado 6
```

Y se verán así:

# Encabezado 1
## Encabezado 2
### Encabezado 3
#### Encabezado 4
##### Encabezado 5
###### Encabezado 6

## Formato de texto
### Negrita y Cursiva

- **Negrita**: Se logra utilizando dos asteriscos `**` o dos guiones bajos `__` al inicio y al final de la palabra o frase.
- *Cursiva*: Se logra utilizando un asterisco `*` o un guión bajo `_` al inicio y al final de la palabra o frase.

```markdown
**Negrita**
__Negrita__
*Cursiva*
_Cursiva_
**_Negrita y Cursiva_**
```

Y se verán así:
- **Este texto está en negrita**
- __Este texto también está en negrita__
- *Este texto está en cursiva*
- _Este texto también está en cursiva_
- **_Este texto está en negrita y cursiva_**

## Listas

### Listas Desordenadas

Utiliza guiones (`-`), asteriscos (`*`), o signoas más (`+`) para crear listas desordenadas.

```markdown
- Elemento 1
- Elemento 2
  - Sub-elemento 2.1
  - Sub-elemento 2.2
- Elemento 3
```

Y se verán así:
- Elemento 1
- Elemento 2
  - Sub-elemento 2.1
  - Sub-elemento 2.2    
- Elemento 3

### Listas Ordenadas

Utiliza números seguidos de un punto para crear listas ordenadas.

```markdown
1. Elemento 1
2. Elemento 2
    1. Sub-elemento 2.1
    2. Sub-elemento 2.2
3. Elemento 3
```
y se verán así:
1. Elemento 1
2. Elemento 2
    1. Sub-elemento 2.1
    2. Sub-elemento 2.2
3. Elemento 3

### Listas de Tareas (To-Do)

Utiliza corchetes cuadrados `[ ]` para crear listas de tareas.

```markdown
- [x] Tarea completada
- [ ] Tarea pendiente
- [ ] Otra tarea pendiente
```

Y se verán así:
- [x] Tarea completada
- [ ] Tarea pendiente
- [ ] Otra tarea pendiente

## Enlaces e Imágenes

### Enlaces

Permite crear hipervínculos a otras páginas o recursos.

```markdown
[Texto del enlace](https://www.ejemplo.com)
```

Y se verán así:
[Texto del enlace](https://www.ejemplo.com)

### Imágenes

Inserta imágenes desde una URL o una ruta local.

```markdown
![Descripción de la imagen](https://placehold.co/400x200)
```

Y se verán así:
![Descripción de la imagen](https://placehold.co/400x200)

## Bloques de Código

### Código en Línea

Utiliza comillas invertidas (`) para resaltar código en línea.

```markdown
`console.log('Hola, Mundo!')`
```

Y se verá así:
`console.log('Hola, Mundo!')`

### Bloques de Código

Utiliza tres comillas invertidas (```) para crear bloques de código.

```markdown
```javascript
function saludar(nombre) {
    return `Hola, ${nombre}!`;
}
```

Y se verá así:

```javascript
function saludar(nombre) {
    return `Hola, ${nombre}!`;
}
```

## Citas 

Utiliza el signo mayor que (`>`) para crear citas.

```markdown
> Esto es una cita.
```

Y se verá así:
> Esto es una cita.

## Tablas

Crea tablas utilizando barras verticales (`|`) y guiones (`-`).

```markdown
| Encabezado 1 | Encabezado 2 | Encabezado 3 |
|--------------|--------------|--------------|
| Fila 1       | Dato 1.1     | Dato 1.2     |
| Fila 2       | Dato 2.1     | Dato 2.2     |
| Fila 3       | Dato 3.1     | Dato 3.2     |
```

Y se verá así:

| Encabezado 1 | Encabezado 2 | Encabezado 3 |
|--------------|--------------|--------------|
| Fila 1       | Dato 1.1     | Dato 1.2     |
| Fila 2       | Dato 2.1     | Dato 2.2     |
| Fila 3       | Dato 3.1     | Dato 3.2     |

## Elementos Multimedia

### Videos de YouTube

Puedes insertar videos de YouTube utilizando el shortcode `youtube`.

```markdown
{{< youtube video_id >}}
```

Y se verá así:
{{<youtube dQw4w9WgXcQ >}}

## Diagramas y Gráficos

Puedes crear diagramas y gráficos mediante el uso de Mermaid y un shortcode en Hugo.

### Diagrama de Flujo

{{< mermaid >}}
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
{{< /mermaid >}}

### Diagrama de Secuencia

{{< mermaid >}}
sequenceDiagram
  participant Cliente
  participant Servidor
  participant BaseDeDatos

  Cliente->>Servidor: Solicitud de datos
  Servidor->>BaseDeDatos: Consulta de datos
  BaseDeDatos-->>Servidor: Datos encontrados
  Servidor-->>Cliente: Respuesta con datos
  Cliente->>Servidor: Confirmación de recepción
  Servidor-->>BaseDeDatos: Actualización de estado
{{< /mermaid >}}
