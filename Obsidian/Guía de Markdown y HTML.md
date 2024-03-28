Los títulos en Obsidian se escriben con un # seguido de un espacio.

# Título nivel 1
## Título nivel 2
### Título nivel 3
#### Título nivel 4
##### Título nivel 5
###### Título nivel 6

# Ctrl + F para buscar

# Formateo del texto
**negrita** y __negrita__
*cursiva* y _cursiva_
***negrita y cursiva***
___negrita y cursiva___
==resaltado==
~~tachar texto~~ - un carácter especial: ~~ (pulsar dos veces: Alt Gr + 4) 

Markdown no permite el subrayado para no confundirlo con los enlaces, aunque con HTML se puede conseguir.

Markdown tampoco permite tener más de dos líneas en blanco. Si esto pasa, se verán en previsualización como una, como un simple espacio.

# Divisores y presentaciones
Los divisores se crean con tres guiones seguidos. Podríamos crear presentaciones siempre y cuando cada diapositiva esté delimitada por 2 divisores.

![[Hola-Mundo.png|443]]

---

presentación 1
texto de la presentación 1

---

presentación 2
texto de la presentación 2

---

<br>

---
---

# Citas
Símbolo de mayor que (>) + espacio + texto de la cita

> Lo importante no es lo que sabes, sino lo que haces con lo que sabes


# Etiquetas
Las etiquetas son palabras (o palabra) que va precedido de una almohadilla (#) sin espacio. Por ejemplo: #To-Do #InProgress #Completed #tag

> Si click en la etiqueta, se nos mostrarán todas las notas que posean dicha etiqueta.


# Listas
## Lista sin numerar
Se crean con un guion + espacio:
- Elemento 1
	- Elemento 1.1
	- Elemento 1.2
		- Elemento 1.2.1
		- Elemento 1.2.2
	- Elemento 1.3
- Elemento 2
	- Elemento 2.1
- Elemento 3


## Lista numerada
Se crean con un número seguido de un punto y de un espacio:
1. Elemento 1
	1. Elemento 1.1
	2. Elemento 1.2
		1. Elemento 1.2.1
		2. Elemento 1.2.2
2. Elemento 2
3. Elemento 3


## Lista mixta (sin y con números)
1. Elemento 1
	- Elemento 1.1
	- Elemento 1.2
		1. Elemento 1.2.1
		2. Elemento 1.2.2
- Elemento 2
- Elemento 3

## Lista de tareas
Se crean con un guión, espacio, abrimos corchetes, dejamos espacio o la marcamos con la x, espacio
- [ ] Tarea 1
	- [x] Tarea 1.1
	- [ ] Tarea 1.2
- [ ] Tarea 2
- [x] Tarea 3
- [ ] Tarea 4

# Imágenes
Si se copia cualquier imagen en el portapapeles y se pega en obsidian, vemos el formato de la imagen, que es ![[]], con el nombre del archivo + su extensión precedida por un punto.

![[Pasted image 20220502170802.png]]

Para redimensionar la imagen ponemos el símbolo barra vertical (| - Alt Gr + 1) seguido del número de píxeles máximos en anchura o altitud, guardando las proporciones de la imagen. Si añadimos nº x nº (anchura x altura) la redimensionaremos a nuestro gusto, sin guardar la proporción original.

![[Hola-Mundo.png|300]]

![[Hola-Mundo.png|250x200]]

Pero si la imagen estuviera fuera del alcance de nuestra bóveda, es decir, si no la tenemos en ninguna carpeta el formato será como un enlace externo precedido de una exclamación (!), haciendo referencia a que está empotrado. Se puede modificar sus dimensiones como lo hemos visto anteriormente.

![Ejemplo](https://i.ytimg.com/vi/MXVefnYC6bY/maxresdefault.jpg)

![Ejemplo|100](https://i.ytimg.com/vi/MXVefnYC6bY/maxresdefault.jpg)


# Bloques código
Para crear bloques de código, tenemos que usar la comilla a la derecha de la P en el teclado español dos veces. Así podemos incluir algún código de lenguajes de programación.

```JavaScript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log(`Hola, mi nombre es ${this.name} y tengo ${this.age} años.`);
  }
}

const person1 = new Person("Juan", 25);
const person2 = new Person("María", 30);

person1.greet(); // Hola, mi nombre es Juan y tengo 25 años.
person2.greet(); // Hola, mi nombre es María y tengo 30 años.

```

# Comentarios para que no compile Markdown
Gracias a no compilar comentarios en Markdown, en el editor vemos dicho comentario pero en previsualización no aparece. Es como un metadato.

%%
	Esto es un comentario hecho por [DanielZ-Code](https://github.com/DanielZ-Code) :)
%%

# Caracteres Markdown que no quieras compilar
Añadir \ (barra invertida - Alt Gr + º) delante del carácter (no detrás):
\[\[no compila]]
\*\*no compila\*\*


# Tablas
| Nombre  | Valor |
|:-------:|:-----:|
| Docena  |  12   |
| Centena |  100  |
|   Mil   | 1000  |
| Dos mil | 2000  |

# Enlaces externos 
## Enlaces externos con Markdown
 - https://obsidian.md/
	 - copiar y pegar directamente una URL
 - [Web de obsidian](https://obsidian.md/)
	 - Seleccionar texto y pulsar Ctrl+K y en el paréntesis () poner la URL
	 - O pulsar Ctrl+K y en los corchetes [] escribir dentro el texto y en el paréntesis () la URL
 - Ctrl+K sale el formato para incluir una url 

## Enlaces externos formato Obsidian
Recurso externo en mi equipo o red local, mediante obsidian, esto no es Markdown:
[Link to note](obsidian://open?path=D:%2Fpath%2Fto%2FLConocimiento-DanielZM.md)


`/` codificados con `%2F` 
` ` Espacios en blanco`%20`


# Enlaces entre notas
## Enlaces entre notas con Markdown
Con caracteres ASCII:

- URL externa de internet
	- [Enlace en línea](https://icon-icons.com)
- ruta de una bóveda como extensión md
	- [Conocimiento](conocimiento.md)
- ruta de mi pc
	- [Ejemplo]("C:\Users\"Nombre"\Desktop\Notas\MiObsidian\Test\Hola.md")

## Enlaces entre notas con wikilinks
Se crean escribiendo dos \[\[ seguido de la nota que queremos hipervincular o enlazar y la seleccionamos.

Ej.: [[Guía de Markdown y HTML]]

Se puede cambiar el nombre de un link [[Guía de Markdown y HTML|si ponemos barra vertical dentro del nombre de la nota y después del último carácter de esta]].

[Más info](https://github.com/agathauy/wikilinks-to-mdlinks-obsidian)

## Transclusiones o notas empotradas (embeded) vs links
Archivo empotrado: \!\[\[GUÍA - Reglas de Markdown y HTML]] - el archivo o nota se ve directamente en la nota, no hace falta salir de obsidian para ir a buscar el archivo o nota.

Link \[\[nota]] - vemos un link que si pinchamos nos conduce al archivo (en la ruta en la que existe).

Podemos decir con un # detrás del último carácter de la nota que queremos que la nota empiece o se vea desde un cabezado en específico, así no perderemos tiempo buscando el encabezado que queremos.

Link: \[\[Titulo#tituloencabezado]]

# Footnotes o notas a pie de página
Ahora les[^nota2] enseño el "código" dentro[^nota1] de Obsidian para hacer una nota ejemplar. [^nota1]

[^nota1]: Esto es una nota de pie de página normal.
[^nota2]: Nota 2: Algo no tan común

# Info extra
- Podemos poner enlaces a notas en encabezados