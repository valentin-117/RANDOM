# RANDOM
#Practica 5 de trabajo en clase

#Se imprime el nombre del autor 
print("FRIAS VILLA ANGEL VALENTIN3W")
#Imprime un espacio en blanco
print("")
#Nombre del programa 
print("Programa que pide al usuario adivinar el numero almacenado")
#Imprime una linea en blanco
print("")

# Importar la librería random para generar un número aleatorio
import random # type: ignore

# Inicializar el contador de intentos
intentos = 0

# Solicitar el nombre del usuario
print("¿Cuál es tu nombre?")
nombre = input()  # Captura el nombre del usuario

# Generar un número aleatorio entre 1 y 50
x = random.randint(1, 50)

# Saludo al usuario e introducción al juego
print("Hola " + nombre + ", vamos a jugar. Tienes solo 5 intentos.")

# Bucle que permite al usuario adivinar el número
while intentos < 5:
    intentos += 1  # Incrementar el contador de intentos

    # Solicitar al usuario que elija un número
    print("Elige un número del 1 al 50")
    numero = input()  # Captura la entrada del usuario
    numero = int(numero)  # Convertir la entrada a un entero
    
    # Comparar el número ingresado con el número secreto
    if x < numero:
        print("El número es menor")  # Indicar que el número es menor
        print("Llevas %d intentos" % (intentos))  # Mostrar la cantidad de intentos

    if x > numero:
        print("El número es mayor")  # Indicar que el número es mayor
        print("Llevas %d intentos" % (intentos))  # Mostrar la cantidad de intentos

    if numero == x:
        break  # Salir del bucle si el usuario adivina el número

# Mensajes finales basados en si el usuario adivinó el número
if numero == x:
    print("!HAS GANADO UNA SKIBIDIGIRL¡")  # Felicitar al usuario por adivinar correctamente
    print(nombre + " lo lograste con %d intentos" % (intentos))  # Mostrar el número de intentos

if numero != x:
    print("Has perdido, vuelve a jugar")  # Mensaje de pérdida
    ![image](https://github.com/user-attachments/assets/969bbb3f-c077-4809-8e75-925c9ba716b0)
