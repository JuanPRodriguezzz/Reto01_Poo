# Reto01_Poo
Crear una función que realice operaciones básicas (suma, resta, multiplicación, división) entre dos números, según la elección del usuario, la forma de entrada de la función será los dos operandos y el caracter usado para la operación. entrada: (1,2,"+"), salida (3).
from subprocess import call

def limpiar_pantalla(): #Función para limpiar la consola
    call("cls",shell=True)

def continuar(): # Función para limpiar la consola dando Enter
    input("\nEnter para continuar")
    call("cls",shell=True)

def operaciones_basicas(num1,num2,operador):
    while True:     
        if operador == '+':
            Resultado = num1 + num2
        elif operador == '-':
            Resultado = num1 - num2
        elif operador == '*':
            Resultado = num1 * num2
        elif operador == '/':
            if num2 != 0:
                Resultado = num1 / num2
            else:
                print("\nNo se puede dividir por cero.\n")
                break
        else:
            print("\n\nIntente de nuevo\n")
            continuar()
            break
        print(f"\n\n{num1} {operador} {num2} = {Resultado}\n")
        break
        
        
while True:
    limpiar_pantalla()
    num1,num2,operador = input("\nIngrese el 1er número, el 2do y el operador separados por comas, (num1,num2,op): ").split(',')
    num1=float(num1)
    num2=float(num2)
    operador=str(operador)
    operaciones_basicas(num1,num2,operador)
    continuar()
    continue
