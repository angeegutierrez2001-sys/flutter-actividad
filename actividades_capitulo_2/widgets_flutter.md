# Investigación de widgets fundamentales en Flutter

**Nombre del estudiante:** Angee Argel<br>
**Curso:** Desarrollo de aplicaciones móviles<br>
**Fecha:** 22 de mayo de 2026<br>

---

## 1. `Container`

### Descripción

El widget `Container` es uno de los widgets más utilizados en Flutter. Se usa para crear una caja o contenedor visual que puede almacenar otro widget dentro de él mediante la propiedad `child`.

Este widget es útil cuando se desea modificar el tamaño, color, margen, relleno, alineación o decoración de un elemento en la interfaz. Por ejemplo, puede utilizarse para crear tarjetas simples, secciones de una pantalla, botones personalizados o bloques visuales con color de fondo.

En términos generales, `Container` permite organizar y personalizar visualmente otros widgets dentro de una aplicación Flutter.

### Ejemplo de código

```dart
Container(
  width: 200,
  height: 100,
  color: Colors.blue,
  alignment: Alignment.center,
  child: Text(
    'Hola Flutter',
    style: TextStyle(
      color: Colors.white,
      fontSize: 20,
    ),
  ),
)
```

### Explicación del ejemplo

En este ejemplo, el `Container` tiene un ancho de `200` píxeles y una altura de `100` píxeles. Su color de fondo es azul y el texto se encuentra centrado gracias a la propiedad `alignment`.

Dentro del `Container` se utiliza la propiedad `child` para incluir un widget `Text`, el cual muestra el mensaje `Hola Flutter`.

### Personalización

El widget `Container` permite modificar diferentes propiedades para cambiar su apariencia y comportamiento. Algunas de las más importantes son:

| Propiedad | Descripción | Ejemplo |
|---|---|---|
| `width` | Define el ancho del contenedor. | `width: 200` |
| `height` | Define la altura del contenedor. | `height: 100` |
| `color` | Cambia el color de fondo. | `color: Colors.blue` |
| `alignment` | Alinea el contenido interno. | `alignment: Alignment.center` |
| `padding` | Agrega espacio interno. | `padding: EdgeInsets.all(16)` |
| `margin` | Agrega espacio externo. | `margin: EdgeInsets.all(10)` |
| `child` | Permite insertar otro widget dentro del contenedor. | `child: Text('Hola')` |
| `decoration` | Agrega bordes, sombras y esquinas redondeadas. | `decoration: BoxDecoration(...)` |

### Ejemplo con personalización

```dart
Container(
  width: 250,
  height: 120,
  margin: EdgeInsets.all(16),
  padding: EdgeInsets.all(20),
  alignment: Alignment.center,
  decoration: BoxDecoration(
    color: Colors.green,
    borderRadius: BorderRadius.circular(15),
    boxShadow: [
      BoxShadow(
        color: Colors.black26,
        blurRadius: 6,
        offset: Offset(2, 4),
      ),
    ],
  ),
  child: Text(
    'Contenedor personalizado',
    style: TextStyle(
      color: Colors.white,
      fontSize: 18,
      fontWeight: FontWeight.bold,
    ),
  ),
)
```

### Explicación de la personalización

En este ejemplo personalizado, el `Container` tiene margen externo, relleno interno, bordes redondeados y una sombra. Además, se utiliza `BoxDecoration` para aplicar una decoración más completa al contenedor.

Este tipo de personalización es útil cuando se desea construir elementos visuales más atractivos, como tarjetas, bloques informativos o secciones destacadas dentro de una pantalla.

### Conclusión

El widget `Container` es fundamental en Flutter porque permite estructurar y personalizar elementos visuales. Su uso es frecuente en casi cualquier interfaz, ya que ayuda a controlar el diseño, el tamaño, los colores, los espacios y la apariencia general de los componentes.

---

## 2. `Text`

### Descripción

El widget `Text` se utiliza para mostrar texto dentro de una aplicación Flutter. Es uno de los widgets más básicos y esenciales para presentar información al usuario.

Puede utilizarse para títulos, descripciones, botones, mensajes y cualquier contenido escrito dentro de la interfaz.

### Ejemplo de código

```dart
Text(
  'Bienvenido a Flutter',
)
```

### Explicación del ejemplo

El widget `Text` muestra el mensaje “Bienvenido a Flutter” en la pantalla de la aplicación.

### Personalización

| Propiedad | Descripción | Ejemplo |
|---|---|---|
| `style` | Modifica la apariencia del texto. | `style: TextStyle(fontSize: 20)` |
| `textAlign` | Define la alineación del texto. | `textAlign: TextAlign.center` |
| `maxLines` | Limita el número de líneas. | `maxLines: 2` |
| `overflow` | Controla el desbordamiento. | `overflow: TextOverflow.ellipsis` |

### Ejemplo con personalización

```dart
Text(
  'Texto personalizado',
  textAlign: TextAlign.center,
  style: TextStyle(
    fontSize: 24,
    color: Colors.purple,
    fontWeight: FontWeight.bold,
  ),
)
```

### Explicación de la personalización

En este ejemplo el texto tiene un tamaño mayor, color púrpura, alineación centrada y estilo en negrita.

### Conclusión

El widget `Text` es importante porque permite mostrar información de forma clara y personalizable dentro de cualquier aplicación Flutter.

---

## 3. `Row`

### Descripción

El widget `Row` organiza widgets hijos de manera horizontal. Es útil para colocar elementos uno al lado del otro dentro de la interfaz.

Se utiliza frecuentemente para menús, barras de navegación, grupos de botones e íconos.

### Ejemplo de código

```dart
Row(
  children: [
    Icon(Icons.star),
    Text('Favorito'),
  ],
)
```

### Explicación del ejemplo

El ejemplo muestra un ícono de estrella junto al texto “Favorito” organizados horizontalmente.

### Personalización

| Propiedad | Descripción | Ejemplo |
|---|---|---|
| `children` | Lista de widgets internos. | `children: []` |
| `mainAxisAlignment` | Distribuye los elementos horizontalmente. | `MainAxisAlignment.spaceAround` |
| `crossAxisAlignment` | Alinea verticalmente los widgets. | `CrossAxisAlignment.center` |

### Ejemplo con personalización

```dart
Row(
  mainAxisAlignment: MainAxisAlignment.spaceAround,
  children: [
    Icon(Icons.home, color: Colors.blue),
    Icon(Icons.search, color: Colors.red),
    Icon(Icons.person, color: Colors.green),
  ],
)
```

### Explicación de la personalización

En este ejemplo los íconos están distribuidos uniformemente en la fila y cada uno tiene un color diferente.

### Conclusión

El widget `Row` facilita la organización horizontal de elementos y ayuda a construir interfaces ordenadas y funcionales.

---

## 4. `Column`

### Descripción

El widget `Column` organiza widgets hijos de forma vertical. Es ideal para formularios, listas de opciones y estructuras en bloques.

### Ejemplo de código

```dart
Column(
  children: [
    Text('Nombre'),
    Text('Correo'),
  ],
)
```

### Explicación del ejemplo

El código muestra dos textos organizados uno debajo del otro.

### Personalización

| Propiedad | Descripción | Ejemplo |
|---|---|---|
| `children` | Lista de widgets internos. | `children: []` |
| `mainAxisAlignment` | Distribuye elementos verticalmente. | `MainAxisAlignment.center` |
| `crossAxisAlignment` | Alinea horizontalmente los widgets. | `CrossAxisAlignment.start` |

### Ejemplo con personalización

```dart
Column(
  mainAxisAlignment: MainAxisAlignment.center,
  crossAxisAlignment: CrossAxisAlignment.start,
  children: [
    Text('Usuario'),
    Text('Contraseña'),
    ElevatedButton(
      onPressed: () {},
      child: Text('Ingresar'),
    ),
  ],
)
```

### Explicación de la personalización

En este ejemplo los elementos están alineados verticalmente y el botón se encuentra debajo de los textos.

### Conclusión

El widget `Column` es esencial para organizar información de manera vertical y mejorar la estructura visual de la interfaz.

---

## 5. `ElevatedButton`

### Descripción

El widget `ElevatedButton` se utiliza para crear botones con relieve y estilo moderno en Flutter.

Estos botones permiten ejecutar acciones cuando el usuario interactúa con ellos.

### Ejemplo de código

```dart
ElevatedButton(
  onPressed: () {
    print('Botón presionado');
  },
  child: Text('Presionar'),
)
```

### Explicación del ejemplo

El botón muestra el texto “Presionar” y ejecuta una acción cuando el usuario hace clic sobre él.

### Personalización

| Propiedad | Descripción | Ejemplo |
|---|---|---|
| `onPressed` | Acción que ejecuta el botón. | `onPressed: () {}` |
| `child` | Widget interno del botón. | `child: Text('Enviar')` |
| `style` | Personaliza la apariencia. | `style: ElevatedButton.styleFrom(...)` |

### Ejemplo con personalización

```dart
ElevatedButton(
  onPressed: () {},
  style: ElevatedButton.styleFrom(
    backgroundColor: Colors.orange,
    padding: EdgeInsets.symmetric(
      horizontal: 30,
      vertical: 15,
    ),
  ),
  child: Text(
    'Botón personalizado',
    style: TextStyle(fontSize: 18),
  ),
)
```

### Explicación de la personalización

En este ejemplo el botón tiene color naranja, mayor espacio interno y un texto con tamaño personalizado.

### Conclusión

El widget `ElevatedButton` es importante porque permite crear interacciones dinámicas y mejorar la experiencia del usuario dentro de la aplicación.

---

# Conclusión general

Los widgets son la base fundamental de Flutter y permiten construir aplicaciones móviles modernas, organizadas y dinámicas.

Widgets como `Container`, `Text`, `Row`, `Column` y `ElevatedButton` facilitan la creación de interfaces visuales funcionales y personalizables.

Conocer el funcionamiento de estos widgets es esencial para desarrollar aplicaciones eficientes y atractivas en Flutter.
---

## 6. `Image`

### Descripción

El widget `Image` se utiliza para mostrar imágenes dentro de una aplicación Flutter. Permite cargar imágenes desde archivos locales, internet o recursos del proyecto.

Es muy útil para mostrar fotografías, logotipos, íconos personalizados, banners y contenido visual dentro de la interfaz.

### Ejemplo de código

```dart
Image.network(
  'https://flutter.dev/images/flutter-logo-sharing.png',
)
```

### Explicación del ejemplo

En este ejemplo se carga una imagen desde internet utilizando `Image.network`. La imagen se mostrará automáticamente dentro de la interfaz de la aplicación.

### Personalización

| Propiedad | Descripción | Ejemplo |
|---|---|---|
| `width` | Define el ancho de la imagen. | `width: 200` |
| `height` | Define la altura de la imagen. | `height: 100` |
| `fit` | Ajusta cómo se adapta la imagen. | `fit: BoxFit.cover` |
| `alignment` | Alinea la imagen. | `alignment: Alignment.center` |

### Ejemplo con personalización

```dart
Image.network(
  'https://flutter.dev/images/flutter-logo-sharing.png',
  width: 250,
  height: 150,
  fit: BoxFit.cover,
)
```

### Explicación de la personalización

En este ejemplo la imagen tiene un ancho y altura definidos. Además, la propiedad `fit` permite ajustar la imagen correctamente dentro del espacio disponible.

### Conclusión

El widget `Image` es importante porque permite agregar contenido visual atractivo y mejorar la experiencia del usuario dentro de una aplicación Flutter.
