---
slug: Diagrams-mermaid
title: Diagramas UML en Markdown
authors: enry6tz
tags: [ docusaurus]
---

Mermaid es una herramienta poderosa que permite generar diagramas directamente desde archivos Markdown en Docusaurus. En esta guía, te mostraré cómo agregar diagramas de clases, entidad-relación (ERD) y diagramas de casos de uso en tus documentos.

<!-- truncate -->

## Diagramas de Clases

Los diagramas de clases son una representación estructural de los objetos en un sistema y sus relaciones. Aquí te muestro cómo puedes definir un diagrama de clases en Markdown usando Mermaid:

```mermaid
classDiagram
    class Blog {
        +String title
        +String content
        +Date publishDate
        +String[] tags
        +Author author
        +Comment[] comments
        +getExcerpt() String
    }

    class Author {
        +String name
        +String bio
        +String profilePicture
        +Blog[] blogs
        +getFullName() String
    }

    class Comment {
        +String text
        +Date commentDate
        +User user
        +Reply[] replies
        +getSummary() String
    }

    class User {
        +String username
        +String email
        +Comment[] comments
        +getProfile() String
    }

    class Reply {
        +String text
        +Date replyDate
        +User user
    }

    Blog "1" --> "1" Author : has
    Blog "1" --> "many" Comment : has
    Comment "1" --> "many" Reply : has
    Comment "1" --> "1" User : by
    Reply "1" --> "1" User : by
    Author "1" --> "many" Blog : writes
    User "1" --> "many" Comment : makes
```

### Explicación

- **Clases**: Definimos clases como `Blog`, `Author`, `Comment`, etc., con sus atributos y métodos.
- **Relaciones**: Indicamos relaciones entre las clases con notaciones como `-->`, que muestran la multiplicidad y el tipo de relación.

## Diagramas de Entidad-Relación (ERD)

Los diagramas de entidad-relación son útiles para modelar bases de datos. Aquí hay un ejemplo básico de cómo puedes crear un ERD con Mermaid:

```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER {
        string name
        string address
    }
    ORDER {
        int orderNumber
        date orderDate
    }
    LINE-ITEM {
        string productCode
        int quantity
        float price
    }
```

### Explicación

- **Entidades**: `CUSTOMER`, `ORDER`, y `LINE-ITEM` representan entidades con atributos.
- **Relaciones**: Se usa `||--o{` para mostrar la relación entre `CUSTOMER` y `ORDER`, y `||--|{` entre `ORDER` y `LINE-ITEM`.

## Diagramas de Casos de Uso

Los diagramas de casos de uso son útiles para representar las interacciones entre actores y el sistema. Aquí tienes un ejemplo sencillo:

```mermaid
graph TB
    actor[User]
    admin[Admin]
    
    actor --> |"Login"| login[Login]
    actor --> |"Browse Products"| browse[Browse Products]
    actor --> |"Place Order"| order[Place Order]
    admin --> |"Manage Products"| manage[Manage Products]
    admin --> |"View Reports"| reports[View Reports]

```



### Explicación
- Actores: Se utilizan nodos etiquetados como actor y admin para representar los actores.
- Casos de Uso: Cada caso de uso se define como un nodo (ej. Login, Browse Products).
- Relaciones: Las flechas (-->) indican la interacción entre los actores y los casos de uso.


En Mermaid, un diagrama de interacción se puede crear utilizando un **diagrama de secuencia** (Sequence Diagram). Este tipo de diagrama es útil para representar la interacción entre diferentes objetos o entidades en un sistema a lo largo del tiempo.

### Ejemplo de Diagrama de Secuencia en Mermaid

```mermaid
sequenceDiagram
    participant Usuario
    participant Sistema
    participant BaseDeDatos

    Usuario->>Sistema: Enviar solicitud
    Sistema-->>Usuario: Confirmar recepción
    Sistema->>BaseDeDatos: Consultar datos
    BaseDeDatos-->>Sistema: Enviar datos
    Sistema-->>Usuario: Mostrar resultados
```

### Explicación

- **`participant`**: Define las entidades o actores que participan en la interacción (ej. `Usuario`, `Sistema`, `BaseDeDatos`).
- **`->>`**: Representa un mensaje o acción enviada de un participante a otro.
- **`-->>`**: Representa una respuesta o retorno de un mensaje.

### Elementos Clave en Diagramas de Secuencia

- **Mensajes Sincrónicos** (`->>`): Indican que el emisor espera una respuesta antes de continuar.
- **Mensajes Asincrónicos** (`-->`): Indican que el emisor no espera una respuesta inmediata y puede continuar procesando.
- **Notas**: Puedes añadir notas al diagrama para clarificar ciertos aspectos.

### Ejemplo con Notas

```mermaid
sequenceDiagram
    participant Cliente
    participant Servidor
    participant API
    Cliente->>Servidor: Solicita información
    note right of Servidor: Procesando solicitud
    Servidor->>API: Consulta la API
    API-->>Servidor: Devuelve datos
    Servidor-->>Cliente: Entrega información
    note over Cliente,Servidor: Interacción completada
```

### Diagrama de Secuencia con Alternativas (Opciones)

Puedes representar condiciones o alternativas usando el bloque `alt`.

```mermaid
sequenceDiagram
    participant Usuario
    participant Sistema

    Usuario->>Sistema: Inicia sesión
    alt Credenciales válidas
        Sistema-->>Usuario: Acceso concedido
    else Credenciales inválidas
        Sistema-->>Usuario: Acceso denegado
    end
```

- **`alt`**: Inicia un bloque de alternativas.
- **`else`**: Indica la condición alternativa dentro del bloque `alt`.



>Con estos ejemplos, puedes empezar a crear tus propios diagramas directamente en Markdown, lo que facilita la documentación de sistemas complejos y sus interacciones. Mermaid es altamente flexible y soporta muchos otros tipos de diagramas que puedes explorar para mejorar tus documentos técnicos.