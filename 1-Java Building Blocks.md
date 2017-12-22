# Bloques de construcción en Java

---

### **Comprender la estructura de una Clase Java**

En java, una **clase** es el bloque de construcción básico. Cuando se define una clase estás describiendo todas las partes y características de uno de esos bloques.
Un **objeto** es una instancia en tiempo de ejecución de una clase en memoria.

## Campos y métodos
Las clases java tienen dos elementos principales:
- **Métodos** (también llamados _funciones_).
- **Atributos** (también conocidos como _variables_).

La unión de estos elementos es lo que se denomina miembros de una clase. Un ejemplo de una clase java puede ser:
```
1: public class Persona { 
2: }
```
En java existen palabras reservadas (**reserved words**) para que el compilador sea capaz de interpretar lo que estamos haciendo dentro de la clase.

A priori no es necesario saber todas estas palabras reservadas. Pero sí que nos tienen que sonar las más usadas. Una pequeña lista de las más importantes:
<table border="0" cellpadding="0" cellspacing="0" width="100%">
        <tr>
        <td valign="top">
            <ul>
                <li class="texto">abstract</li>
                <li class="texto">assert</li>
                <li class="texto">boolean</li>
                <li class="texto">break</li>
                <li class="texto">byte</li>
                <li class="texto">case</li>
                <li class="texto">catch</li>
                <li class="texto">char </li>
                <li class="texto">class</li>
                <li class="texto">const</li>
            </ul>
        </td>
        <td width="20">&nbsp;</td>
        <td valign="top" width="20%"><ul>
            <li class="texto">continue</li>
            <li class="texto">default</li>
            <li class="texto">do</li>
            <li class="texto">double</li>
            <li class="texto">else </li>
            <li class="texto">enum</li>
            <li class="texto">extends </li>
            <li class="texto">final </li>
            <li class="texto">finally</li>
            <li class="texto">float</li>
        </ul></td>
        <td width="20">&nbsp;</td>
        <td valign="top" width="20%"><ul>
            <li class="texto">for </li>
            <li class="texto">goto</li>
            <li class="texto">if</li>
            <li class="texto">implements</li>
            <li class="texto">import </li>
            <li class="texto">instanceof </li>
            <li class="texto">int </li>
            <li class="texto">interface</li>
            <li class="texto">long </li>
            <li class="texto">native</li>
        </ul></td>
        <td width="20">&nbsp;</td>
        <td valign="top" width="20%"><ul>
            <li class="texto">new         </li>
            <li class="texto">package</li>
            <li class="texto">private</li>
            <li class="texto">protected</li>
            <li class="texto">public </li>
            <li class="texto">return </li>
            <li class="texto">short  </li>
            <li class="texto">static </li>
            <li class="texto">strictfp </li>
            <li class="texto">super </li>
        </ul></td>
        <td width="20">&nbsp;</td>
        <td valign="top" width="20%"><ul>
            <li class="texto">switch</li>
            <li class="texto">synchronized</li>
            <li class="texto">this</li>
            <li class="texto">throw</li>
            <li class="texto">throws</li>
            <li class="texto">transient</li>
            <li class="texto">try</li>
            <li class="texto">void</li>
            <li class="texto">volatile</li>
            <li class="texto">while</li>
        </ul></td>
        </tr>
    </table>

**NOTA**: **NO** se puede crear ninguna _clase_, _variable_, _método_ o _campo_ con estos nombres. Aunque como JAVA es case sensitive sí que puede haber por ejemplo un atributo llamado **Public**, pero no uno llamado **public**.

## Comentarios

Los comentarios son fragmentos de código que no se ejecuta. Hay varios tipos de comentarios:
```java
// Comentarios de una sóla línea

/*
*  Comentarios de varias líneas
*/

/**
*  Comentarios de JavaDoc
*  @author
*/
```

## Clases Vs Ficheros
Cada clase define su propio fichero ***.java**. Normalmente es public, que significa que cualquier código puede llamarlo.
Se puede tener dos clases en el mismo fichero, no es muy habitual pero es correcto. Lo único que hay que tener en cuenta es que si tenemos varias clases en un fichero la clase que coincide con el nombre del fichero debe ser public.
Por ejemplo:
```java
1: public class Animal {
2:   private String name;
3: }
4: class Animal2 {
5: }
```
En este caso debe de existir un fichero se llama **Animal.java**.

## Método main()
El método main en java es un estándar utilizado por la JVM para iniciar la ejecución de cualquier programa Java. Dicho método se conoce como punto de entrada de la aplicación java.
```java
1: public class Animal {
2:  public static void main(String[] args) {
3:
4:  }
5:}
```
Para compilar y ejecutar este código hay que compilar el fichero .java y luego ejecutar la clase:

```java
$ javac Animal.java
$ java Animal
```
Volviendo al método main() lo que hay que tener en cuenta son los siguientes puntos:
- 