# Reto 5

1. Dado la figura de la imagen, desarrolle:

![image](https://github.com/user-attachments/assets/8300fa43-7ae4-494d-9cff-82b22d296726)

* Una función matemática para calcular el volumen y el área superficial.
* Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r1, r2 y h.
* Revise como utilizar el valor de pi usando import math y math.pi

```python
from math import pi, sqrt #se trae de la libreria math especificamente los dos modulos que serán útiles

def calcular_solidos(r1:float, r2:float, h:float) -> float:
    areaEsfera = 4*pi*(r1**2)
    volumenEsfera = 4/3*pi*(r1**2)
    gCono = sqrt((r2**2)+(h**2)) #para el calculo de la superficie del cono se necesita la generatriz del cono, 
    #para esto tomando la generatriz como la hipotenusa se calcula la raiz de la suma de los cuadrados del radio del cono con la altura del cono
    areaCono = pi*r2*(r2+gCono)
    volumenCono = 1/3*pi*(r2**2)*h 
    return areaCono, volumenCono, volumenEsfera, areaEsfera

def ingreso_teclado(r1: float, r2: float, h: float) -> float:
    #funcion para organizar los datos tras el ingreso por teclado en main
    aCono, vCono, vEsfera, aEsfera = calcular_solidos(r1, r2, h)#se llama a la funcion para calcular las areas y volumenes
    aTotal = aCono + aEsfera 
    vTotal = vCono + vEsfera 
    return aTotal, vTotal


if __name__=="__main__":
    radioE = float(input("Ingrese el radio de la esfera. "))
    radioC = float(input("Ingrese el radio de la base del cono. "))
    alturaC = float(input("Ingrese la altura del cono. "))
    areaTotal, volumenTotal = ingreso_teclado(radioE, radioC, alturaC)
    print("El area total de los sólidos es: ", areaTotal, "\nEl volumen total de los sólidos es: ", volumenTotal)

```
2. Dado la figura de la imagen, desarrolle:

![image](https://github.com/user-attachments/assets/69a02987-a896-4f0d-a435-02cfa2fd3460)

* Una función matemática para calcular el área y el perimetro.
* Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r, a y b.
* Revise como utilizar el valor de pi usando import math y math.pi

```python 
from math import pi

def area_perimetro_vagon (r: float, a: float, b: float) -> float:
    perimetro_ruedas = 2*(2*pi*r) #los dos circulos son iguales por lo que se multiplica por dos
    perimetro_vagon = (2*a)+(2*b)
    area_vagon = a*b
    area_ruedas = 2*(pi*(r**2))
    return area_ruedas, area_vagon, perimetro_ruedas, perimetro_vagon

def ingreso_teclado(r: float, a: float, b: float) -> float:
    #funcion para organizar los datos tras el ingreso por teclado en main
    a_ruedas, a_vagon, p_ruedas, p_vagon = area_perimetro_vagon(r, a, b)#se llama a la funcion para calcular las areas y volumenes
    aTotal = a_ruedas + a_vagon 
    pTotal = p_ruedas + p_vagon
    return aTotal, pTotal

if __name__=="__main__":
    radioR = float(input("Ingrese el radio de los circulos. "))
    ancho = float(input("Ingrese el ancho del rectangulo. "))
    altura = float(input("Ingrese la altura del rectangulo. "))
    areaTotal, perimetroTotal = ingreso_teclado(radioR, ancho, altura)
    print("El area total de la superficie es: ", areaTotal, "\nEl perimetro total de la superficie es: ", perimetroTotal)
```

3. Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.
```python
def cantidad_de_carne (N: int, M: int, K: int) -> int:
    kg_gallinas = N * 6
    kg_gallos = M * 7 
    kg_pollitos = K * 1 
    return kg_gallinas, kg_gallos, kg_pollitos

if __name__=="__main__":
    nGallinas = int(input("Ingrese el número de gallinas que tiene: "))
    nGallos = int(input("Ingrese el número de gallos que tiene: "))
    nPollitos = int(input("Ingrese el número de pollitos que tiene: "))
    carGallina, carGallo, carPollito = cantidad_de_carne (nGallinas, nGallos, nPollitos)
    print ("Para un numero de ", nGallinas, " gallinas, hay una cantidad de carne de ", carGallina,"Kg")
    print ("Para un numero de ", nGallos, " gallos, hay una cantidad de carne de ", carGallo,"Kg")
    print ("Para un numero de ", nPollitos, " pollitos, hay una cantidad de carne de ", carPollito,"Kg")
```
4. Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.
```python
```
5. Escriba un programa que pida 5 números reales y calcule las siguientes operaciones usando una función para cada una:

* El promedio
```python
```
* La mediana
```python
```
* El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)
```
```
* La potencia del mayor número elevado al menor número
```python
```
* La raíz cúbica del menor número
```python
```
Para el punto anterior incluir las funciones en un archivo independiente e importarlas para su uso.
```python
```

6. Consultar qué es y cómo funciona pip en python.

7. Hacer un listado de módulos populares para python que se puedan instalar con pip y consultar cómo instalarlos.
