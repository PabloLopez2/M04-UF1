# M04-UF1
Cyber: Llenguatges de Marques (M04 - UF1)

## XML

### Tipos de etiquetas
>**cabecera →** \<?xml version="1.0" encoding="UTF-8" ?>. 
>>Esto indica a nuestro programa o a la librería que utilizamos internamente de programación, que es lo que vamos a leer, qué codificación y que versión del estándar es.

>**Para comentar →** \<!-- texto -->

* Etiquetas pares:
	* Se abren y cierran, Cuando lo que tenemos que escribir es muy variable, puede ser par (character por ejemplo, o cuando algo vaya a contener muchos datos)
* Etiquetas impares:
	* Se cierran en sí mismas. Por ejemplo la edad, es una cosa muy concreta, entonces es recomendable hacerla impar.


### Ejemplo de atributo o propiedad
> **\<age value="197" />** → Value es un atributo o propiedad. Un atributo es una propiedad que se define dentro de la etiqueta de un elemento y proporciona información adicional sobre ese elemento. 
	
*Cosas a tener en cuenta:*

Todo archivo XML, necesita una **etiqueta raíz**, una etiqueta donde dependen el resto de elementos (como el root), lo ideal es que represente algo (ej: character) y toda etiqueta raíz debe cerrarse. 
Eso sí, es importante escribir en inglés, no hay que escribir ñ, ç, ´, (no poner anio, anyo, o ano).

>**UTF-8** → ignifica que incluye todos los carácteres (sistema de codificación universal) incluidos extraterrestres (emojis). 


### Código en XML:
```XML
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE character SYSTEM "character.dtd">
<character id_character="1">
	<name>Eustaquio</name>
	<surname>Mendoza</surname>
	<!-- Comentario -->
	<age value="197" />
	<race>Enano</race>
	<class>Artificiero</class>
	<gender abbrev="N">Non-Binary</gender>
	<height cm="130" />
	<weight kg="80" />
	<language abbrev="prt">Portugués</language>
	<TieneLaEso />
	<weapons>
		<weapon id_weapon="1" />
		<weapon id_weapon="3" />
		<weapon id_weapon="7" />
		<weapon id_weapon="1" />
	</weapons>
</character> 
```



## DTD
### Código en DTD
```DTD
<!ELEMENT character (name, surname, age, race, class, 
	height, weight, language, TieneLaEso, weapons?)>

<!ELEMENT name (#PCDATA)>
<!ELEMENT surname (#PCDATA)>
<!ELEMENT age EMPTY>
<!ELEMENT race (#PCDATA)>
<!ELEMENT class (#PCDATA)>
<!ELEMENT gender (#PCDATA)>
<!ELEMENT height EMPTY>
<!ELEMENT weight EMPTY>
<!ELEMENT language (#PCDATA)>
<!ELEMENT weapons (weapon*)>
<!ELEMENT weapon EMPTY>

<!ATTLIST character id_character CDATA #REQUIRED> 
<!ATTLIST age years CDATA #REQUIRED> 
<!ATTLIST gender abbrev CDATA #REQUIRED> 
<!ATTLIST height cm CDATA #REQUIRED> 
<!ATTLIST weight kg CDATA #REQUIRED> 
<!ATTLIST language abbrev CDATA #REQUIRED> 
```


## MarkDown

### Listas
* uno
	* sub apartado 1
* dos
	* sub apartado 2
* tres
	* sub apartado 3
	
### Citas
> Esto sirve para citar
> para destacar cosas concretas
> como un codiguito
>> Esto es una cita **dentro** de una _cita_ 


---

### Enlaces

Enlace
[CondorChem](https://condorchem.com)

Y [ESTO](http://enti.cat) es otro enlace

### Imagen incrustada
![Descripcion de la imagen](https://5.imimg.com/data5/SJ/GR/TW/SELLER-63202466/ventorlin-inhaler-500x500.jpg)


### Ejemplo de resaltado de sintaxis

```kotlin
fun printOnlyOdds(list: List<Int?>) {

    for (element in list) {
        if ((element?.rem(2) ?: 0) != 0) {  //rem = remainder %
            print("$element ")
        }
    }
}
```

### Listas de tareas
- [ ] Primera tarea
- [X] Segunda tarea
- [ ] Tercera tarea



### Carácteres extendidos
:poop: :alien: :cry: :imp: :relaxed: :laughing: :cherries: :rat:


### Estilo de caracteres

*cursiva* _cursiva_

**negrita** __negrita__

~~TACHADO~~

~~***tachado negrita u cursiva***~~

### Tablas
| id_character | name | age | level |
| ---: | ---: | ---: | ---: |
| 1 | Eustaquio | 197 | 99 |
| 2 | Mariana | 20 | 100 | 
| 3 | Mortadelo | 100 | 1 |
| 4 | Messi | 44 | 99 |


### Escapar caracteres
\# escapar 

\*escapar*

