Funciones predefinidas
======================

.. image:: /logos/logo-python.png
    :scale: 25%
    :alt: Logo Python 
    :align: center

.. |date| date::
.. |time| date:: %H:%M


Funciones básicas de Python 3.8

.. contents:: Índice

Manipulación de variables
#########################

Averiguar tipo de dato
**********************
 
.. code-block:: python
    :linenos:

    cadena = "soy un texto"

    print(type(cadena))


Manipulación de Strings
#######################

Longitud de un String 
*********************

.. code-block:: python
    :linenos:

    nombre = "Guillermo"

    print(len(nombre))

Conversión número a String 
**************************

.. code-block:: python
    :linenos:

    edad = 33

    # Aquí tendríamos un error si no convertimos:
    print("Tienes " + str(edad) + " años.")

Conversión String a Lista
*************************

.. code-block:: python
    :linenos:

    compra = "tomates, lechugas, peras, patatas"

    lista_compra = compra.split(", ")

    print(lista_compra)

Reemplazar palabras
*******************

.. code-block:: python
    :linenos:

    frase = "Soy la persona mas afortunada"

    print(frase.replace('Soy', 'Era'))

Conversión a mayúsculas
***********************

.. code-block:: python
    :linenos:

    frase = "Hace buen día"

    print(frase.upper())

Conversión a minúsculas
***********************

.. code-block:: python
    :linenos:

    frase = "MI nombre Es Alfredo"

    frase = frase.lower()
    print(frase)

Eliminar espacios en blanco a los lados
***************************************

.. code-block:: python
    :linenos:

    frase = "   Soy la persona mas afortunada         "

    print(frase.strip())

Localizar posición de caracteres en cadena
******************************************

.. code-block:: python
    :linenos:

    secreto = "La palabra secreta es Gato"

    # Esto vale para cualquier tipo en Python:
    if "Gato" in secreto:
        print("Descifrado el secreto")
 
Comprobar que no existe un valor
********************************
  
.. code-block:: python
    :linenos:

    # Lista con datos repetidos:
    lista_compra = ['galletas', 'pescado', 'galletas', 'fresas', 'pescado', 'pescado','fresas']

    # lista donde irán valores filtrados:
    lista_unica = []

    # recorrer los datos:
    for compra in lista_compra:
        if compra not in lista_unica:
            lista_unica.append(compra)

    print(lista_unica)

Formatear contenido de una variable con otras
*********************************************
 
.. code-block:: python
    :linenos:
    
    nombre = "Guillermo"
    apellidos = "Granados Gómez"
    edad = 33

    # para formatear cadenas se usa format():
    print("Me llamo {} {} y tengo {} años.".format(nombre, apellidos, str(edad)))

Manipulación de Números
#######################

Conversión String a Integer
***************************

.. code-block:: python
    :linenos:

    numero = int(input("introduce un número: "))
    print(numero + 15)

Conversión String a Float
*************************

.. code-block:: python
    :linenos:

    numero = float(input("introduce un número: "))
    print(numero + 12.6)

Redondeo de decimales
*********************

.. code-block:: python
    :linenos:

    numero = 13.587

    # redondeo a entero:
    print(round(numero))

    # redondear a nivel decimal:
    print(round(numero, 2))


Manipulación de Listas
######################

Comprobar tamaño
****************

.. code-block:: python
    :linenos:

    lista = ["talco", "crema", "gel", "champú"]

    # También se usa len para medir tamaño de una lista:
    print(len(lista))

Imprimir contenido
******************

.. code-block:: python
    :linenos:

    print(lista[1])

Imprimir ultimo valor de la lista
*********************************

.. code-block:: python
    :linenos:

    print(lista[len(lista)-1])

Añadir elemento a la lista
**************************

.. code-block:: python
    :linenos:
  
    lista.append("nuevo texto")
    print lista

Borra el último elemento
************************

.. code-block:: python
    :linenos:

    lista.pop()
    print(lista)

Borrar elemento por su posición
*******************************

.. code-block:: python
    :linenos:

    del lista[2]
    print(lista)

Combinar elementos de la lista en un string
*******************************************

.. code-block:: python
    :linenos:

    lista = ['P','e','p','e']
    lista = ''.join(lista)
    print(lista)

Convertir a lista una serie de valores
**************************************

.. code-block:: python
    :linenos:

    numeros = range(0,30)
    lista = list(numeros)
    print(lista)

Rango de números
****************

.. code-block:: python
    :linenos:

    rango = range(1,11)
    print(list(rango))

Recuperar valor máximo
**********************

.. code-block:: python
    :linenos:

    print(max(rango))

Recuperar valor mínimo
**********************

.. code-block:: python
    :linenos:

    print(min(rango))

Suma total de todos los valores
*******************************

.. code-block:: python
    :linenos:

    print(sum(rango))

Ordenar elementos
*****************

.. code-block:: python 
    :linenos:

    lista = ["gato", "nocilla", "avión", "leche"]

    # Orden normal:
    print(sorted(lista))

    # Orden inverso:
    print(sorted(lista, reverse=True))

.. note::
    En las tuplas podemos usar casi todas las mismas funciones excepto append() y pop() y 
    se cambia el modificador list() por tuple()

Manipulación de Diccionarios 
############################

Convertir a tupla
*****************

.. code-block:: python 
    :linenos:

    tupla = diccionario.items()
    print(tupla)

Copiar un diccionario
*********************

.. code-block:: python
    :linenos:

    otro = diccionario.copy()
    print(otro)

Recuperar solo las claves del diccionarios
******************************************

.. code-block:: python
    :linenos:

    claves = diccionario.keys()
    print(claves)

Recuperar solo los valores del diccionario
******************************************

.. code:: python 
    :linenos:

    valores = diccionario.values()
    print(valores)

Tratamiento de archivos
#######################

**Nomenclatura**  

* Escritura: w 
* Lectura: r 
* Actualización: a 

Manipulación de archivos
************************

* Escritura de archivos:

.. code-block:: python
    :linenos:

    # abrimos el archivo con escritura por ejemplo:
    archivo = open('archivo.txt', 'w')

    # Escribimos varias líneas:
    archivo.write('Hola')
    archivo.write('\n')
    archivo.write('Lo de antes es un salto de línea')

    # Y lo cerramos
    archivo.close()

* Lectura de archivos:

.. code-block:: python
    :linenos:

    archivo = open('archivo.txt', 'r')

    # Y lo guardamos en una lista eliminando los saltos:
    lista = archivo.read().split('\n')

    for l in lista:
        print(l)

    archivo.close()

* Actualización de archivos:

.. code-block:: python
    :linenos:

    archivo = open('archivo.txt', 'a')

    archivo.write('\n')
    archivo.write('linea adicional')

    archivo.close()
