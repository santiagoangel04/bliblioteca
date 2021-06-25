# juego de adivinansas
"""este es un primer programa con una supuesta interfas de usuario, el juego es un proceso tanto de desarrollo mio, aqui no utilizo muchas cosas, pues el fin de este era esforzarme al desarrollo de la interfas"""

#importo las blibiotecas que utilizare, para la interfas utilizare turtle
import turtle
import time
import random

"""cordenada de la locacion, la dejo en variable porque la necesitare despues"""
cordenada_locacion=-300

#creacion de la ventana 
ventana=turtle.Screen()
ventana.title("YESSICA GOTIC")
ventana.setup(width= 1240, height=400)
ventana.bgcolor("grey")
ventana.tracer()

#creacion del lapiz para el escrito
escrito=turtle.Turtle()
escrito.speed(0)
escrito.hideturtle()
escrito.penup()
escrito.goto(0,15)

#creacion del cuadro
cuadro = turtle.Turtle()
cuadro.speed(0)
cuadro.color("green")
cuadro.hideturtle()
cuadro.penup
cuadro.goto(cordenada_locacion,0)
cuadro.pensize(5)
cuadro.pendown()

#variable que alojara los numeros aletorios
numero_aletorio= random.randint(1,10)

"""este bucle me ayudara a recducir el codigo para los trazos del cuadro"""
for i in range(2):
    cuadro.forward(600)
    cuadro.left(90)
    cuadro.forward(50)
    cuadro.left(90)
    
escrito.write("BIENVENIDO A YESSICA GOTIC ",align="center", font=("Arial",20,'normal'))
time.sleep(2)
escrito.clear()
"""aqui hay un tiempo de espera donde se va a limpiar lo escrito en el cuadro, esto para avanzar y que no se queden los escritos ahi y se vea feo"""

#bucle de entrada del jugador

while True:
    y =ventana.textinput("ENTRADA ","si quieres parar escribe 'stop' \n si no escribe 'start': ")
    
#aqui se tomaran la entrada para cerrar o no el juego

    if y == 'start' or y == 'START':
        numero_jugadores=int(ventana.numinput("INICIO DEL JUEGO","numeros de jugadores, el numero maximo de jugadores es 4: ", minval=1, maxval=4))
        if numero_jugadores == 1:
            
            name_1=str(ventana.textinput("JUGADOR 1","cual es tu nombre: "))
            
            cuadro.clear()
            
 #definidor de funcion donde se contaran las letras de la entrada de usuario llamada name_1
            #ademas aqui se implementaran los jugadores
            
            def contador_letras(cadena):
                contador =0

                while cadena[contador:]:
                    contador+=1
                    
                return contador
            
            letras_totales=len(name_1)
            
            if letras_totales >= 5 and letras_totales <= 15:
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)

            if letras_totales >= 15:
                letras_totales=letras_totales + 24
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)
            
            elif letras_totales <=4:
                for i in range(2):
                    cuadro.forward(600)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)
            
            escrito.write("hola, a jugar " + name_1, align="center", font=("courier" ,40,'bold italic'))
            time.sleep(3)
            escrito.clear()

            x = ventana.numinput("JUGADOR 1 ADIVINA","escribe un numero de 1 a 10", minval=1, maxval= 10)

            if x == numero_aletorio:
                escrito.write("GANASTE " + name_1, align="center", font=("courier",40,'bold italic'))
                time.sleep(3)
            else:
                escrito.write("PERDISTE " + name_1, align="center", font=("courier",40,'bold italic'))

        if numero_jugadores == 2:
            
            name_1=str(ventana.textinput("JUGADOR 1","cual es tu nombre: "))
            cuadro.clear()

            def contador_letras(cadena):
                contador =0

                while cadena[contador:]:
                    contador+=1
                    
                return contador
            
            letras_totales=len(name_1)
            
 #con los if se modificaran las medidas del cuadro, esto en variacion a la cantidad de caracteres ingresados en el nombre 
 
            if letras_totales >= 5 and letras_totales <= 15:
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)

            if letras_totales >= 15:
                letras_totales=letras_totales + 24
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)
            
            elif letras_totales <=4:
                for i in range(2):
                    cuadro.forward(600)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)

            escrito.write("hola, a jugar " + name_1, align="center", font=("courier" ,40,'bold italic'))
            time.sleep(3)
            escrito.clear()

            x = ventana.numinput("JUGADOR 1 ADIVINA","escribe un numero de 1 a 10: ", minval= 1 , maxval= 10)

            name_2=str(ventana.textinput("JUGADOR 2 ","cual es tu nombre: "))
            cuadro.clear()

            def contador_letras(cadena):
                contador=0

                while cadena[contador:]:
                    contador+=1
            letras_totales=len(name_2)

            if letras_totales >= 5 and letras_totales <= 15:
                cordenada_ancho = letras_totales * 9
                b = cordenada_ancho // -2
                cordenada_locacion_2 = cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)
                
            if letras_totales >= 15:
                letras_totales= letras_totales + 24
                cordenada_ancho= letras_totales * 9
                b= cordenada_ancho // -2
                cordenada_locacion_2 = cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2, 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)
            
            if letras_totales <= 4:
                for i in range(2):
                    cuadro.forward(600)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)
                
            escrito.write("hola, a jugar " + name_2, align="center", font=("courier" ,40,'bold italic'))
            time.sleep(3)
            escrito.clear()

            z = ventana.numinput("JUGADOR 2 ADIVINA","escribe un numero de 1 a 10: ", minval= 1, maxval=10)

            if x == numero_aletorio and z == numero_aletorio:
                escrito.color("yellow")
                escrito.write("los jugadores empatan ", align="center", font=("courier",40,'bold italic'))
                time.sleep(4)
                escrito.clear()

            elif x == numero_aletorio or z == numero_aletorio:
                if x == numero_aletorio:
                    escrito.color("yellow")
                    escrito.write("el jugador " + name_1 + "GANA" , align="center", font=("courier",40,'bold italic'))
                    time.sleep(4)
                    escrito.clear()

                if z == numero_aletorio:
                    escrito.color("yellow")
                    escrito.write("el jugador " + name_1 + "GANA", align="center", font=("courier",40,'bold italic'))
                    time.sleep(4)
                    escrito.clear()

            if x != numero_aletorio and z != numero_aletorio:
                escrito.color("red")
                escrito.write("los dos pierden", align="center", font=("courier",40,'bold italic'))
                time.sleep(4)
                escrito.clear()

            elif x != numero_aletorio or z != numero_aletorio:
                if x != numero_aletorio:
                    escrito.color("red")
                    escrito.write("el jugador" + name_1 + "PIERDE", align="center", font=("courier",40,'bold italic'))
                    time.sleep(4)
                    escrito.clear()

                if x != numero_aletorio:
                    escrito.color("red")
                    escrito.write("el jugador " + name_1 + "PIERDE", align="center", font=("courier",40,'bold italic'))
                    time.sleep(4)
                    escrito.clear()

        escrito.color("black")

        if numero_jugadores == 3:

            name_1=str(ventana.textinput("JUGADOR 1","cual es tu nombre: "))
            cuadro.clear()

            def contador_letras(cadena):
                contador =0

                while cadena[contador:]:
                    contador+=1
                    
                return contador
            
            letras_totales=len(name_1)
            
            if letras_totales >= 5 and letras_totales <= 15:
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)

            if letras_totales >= 15:
                letras_totales=letras_totales + 24
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)
            
            elif letras_totales <=4:
                for i in range(2):
                    cuadro.forward(600)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)

            escrito.write("hola, a jugar " + name_1, align="center", font=("courier" ,40,'bold italic'))
            time.sleep(3)
            escrito.clear()

            x = ventana.numinput("JUGADOR 1 ADIVINA" , "escribe un numero de 1 a 10: ", minval= 1 , maxval= 10)

            name_2=str(ventana.textinput("JUGADOR 2","cual es tu nombre: "))
            cuadro.clear()
            time.sleep(3)
            escrito.clear()

            def contador_letras(cadena):
                contador =0

                while cadena[contador:]:
                    contador+=1
                    
                return contador
            
            letras_totales=len(name_2)
            
            if letras_totales >= 5 and letras_totales <= 15:
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)

            if letras_totales >= 15:
                letras_totales=letras_totales + 24
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)
            
            elif letras_totales <=4:
                for i in range(2):
                    cuadro.forward(600)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)

            escrito.write("hola, a jugar " + name_2, align="center", font=("courier" ,40,'bold italic'))
            time.sleep(3)
            escrito.clear()
            
            z = ventana.numinput("JUGADOR 2 ADIVINA","escribe un numero de 1 a 10: ", minval=1 , maxval= 10)
            
            name_3 =str(ventana.textinput("JUGADOR 3","cual es tu nombre: "))
            cuadro.clear()
            time.sleep(3)
            escrito.clear()

            def contador_letras(cadena):
                contador =0

                while cadena[contador:]:
                    contador+=1
                    
                return contador
            
            letras_totales=len(name_3)
            
            if letras_totales >= 5 and letras_totales <= 15:
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)

            if letras_totales >= 15:
                letras_totales=letras_totales + 24
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)
            
            elif letras_totales <=4:
                for i in range(2):
                    cuadro.forward(600)
                    cuadro.left(90)
                    cuadro.forward(70)
                    cuadro.left(90)

            escrito.write("hola, a jugar " + name_3, align="center", font=("courier" ,40,'bold italic'))
            time.sleep(3)
            escrito.clear()

            m = ventana.numinput("JUGADOR 3 ADIVINA","escribe un numero de 1 a 10: ", minval=1, maxval=10)
           
            if x == numero_aletorio and z == numero_aletorio and m == numero_aletorio:
                escrito.color("yellow")
                escrito.write("los 3 jugadores ganan", align="center", font=("courier",40,'bold italic'))
            
            elif x == numero_aletorio or z == numero_aletorio or m == numero_aletorio:
                if x == numero_aletorio:
                    escrito.color("yellow")
                    escrito.write("el jugador 1 gana", align="center", font=("courier",40,'bold italic'))
                    time.sleep(4)
                    escrito.clear()

                elif z == numero_aletorio:
                    escrito.color("yellow")
                    escrito.write("el jugador 2 gana", align="center", font=("courier",40,'bold italic'))
                    time.sleep(4)
                    escrito.clear()

                elif m == numero_aletorio:
                    escrito.color("yellow")
                    escrito.write("el jugador 3 gana", align="center", font=("courier",40,'bold italic'))
                    time.sleep(4)
                    escrito.clear()
            
            if x != numero_aletorio and z != numero_aletorio and m != numero_aletorio:
                escrito.color("red")
                escrito.write("los 3 jugadores pierden", align="center", font=("courier",40,'bold italic'))
                time.sleep(4)
                escrito.clear()

            elif x != numero_aletorio or z != numero_aletorio or m != numero_aletorio:
                if x != numero_aletorio:
                    escrito.color("red")
                    escrito.write("el jugador 1 pierde", align="center", font=("courier",40,'bold italic'))
                    time.sleep(4)
                    escrito.clear()

                elif z != numero_aletorio:
                    escrito.color("red")
                    escrito.write("el jugador 2 pierde", align="center", font=("courier",40,'bold italic'))
                    time.sleep(4)
                    escrito.clear()

                elif m != numero_aletorio:
                    escrito.color("red")
                    escrito.write("el jugador 3 pierde", align="center", font=("courier",40,'bold italic'))
                    time.sleep(4)
                    escrito.clear()

            elif z == numero_aletorio and x == numero_aletorio and m == numero_aletorio:
                escrito.color("black")
                escrito.write("los tres jugadores estan empatados", align="center", font=("Arial",40,'normal'))
        
        escrito.color("black")

        if numero_jugadores == 4:
            name_1=str(ventana.textinput("JUGADOR 4""cual es tu nombre: "))

            def contador_letras(cadena):
                contador =0

                while cadena[contador:]:
                    contador+=1
                    
                return contador
            
            letras_totales=len(name_1)
            
            if letras_totales >= 5 and letras_totales <= 15:
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)

            if letras_totales >= 15:
                letras_totales=letras_totales + 24
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)
            
            elif letras_totales <=4:
                for i in range(2):
                    cuadro.forward(600)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)
            x = int(input("escribe un numero de 1 a 10: "))

            name_2=str(input("cual es tu nombre: "))
            print("usted sera el jugador 2 ")

            def contador_letras(cadena):
                contador =0

                while cadena[contador:]:
                    contador+=1
                    
                return contador
            
            letras_totales=len(name_2)
            
            if letras_totales >= 5 and letras_totales <= 15:
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)

            if letras_totales >= 15:
                letras_totales=letras_totales + 24
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)
            
            elif letras_totales <=4:
                for i in range(2):
                    cuadro.forward(600)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)
            
            z = int(input("escribe un numero de 1 a 10: "))
            
            name_3 =str(input("cual es tu nombre: "))
            print("usted sera el jugador 3 ")

            def contador_letras(cadena):
                contador =0

                while cadena[contador:]:
                    contador+=1
                    
                return contador
            
            letras_totales=len(name_3)
            
            if letras_totales >= 5 and letras_totales <= 15:
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)

            if letras_totales >= 15:
                letras_totales=letras_totales + 24
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)
            
            elif letras_totales <=4:
                for i in range(2):
                    cuadro.forward(600)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)
            m = int(input("escribe un numero de 1 a 10: "))

            name_4 =str(input("cual es tu nombre: "))
            print("usted sera el jugador 4 ")

            def contador_letras(cadena):
                contador =0

                while cadena[contador:]:
                    contador+=1
                    
                return contador
            
            letras_totales=len(name_4)
            
            if letras_totales >= 5 and letras_totales <= 15:
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)

            if letras_totales >= 15:
                letras_totales=letras_totales + 24
                cordenada_ancho= letras_totales * 9 
                b= cordenada_ancho // -2
                cordenada_locacion_2= cordenada_locacion + b
                cuadro.goto(cordenada_locacion_2 , 0)

                for i in range(2):
                    cuadro.forward(600 + cordenada_ancho)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)
            
            elif letras_totales <=4:
                for i in range(2):
                    cuadro.forward(600)
                    cuadro.left(90)
                    cuadro.forward(50)
                    cuadro.left(90)
            n = int(input("escribe un numero de 1 a 10:"))

           
            if x == numero_aletorio:
                print("el jugador 1 gana")
            
            if x != numero_aletorio:
                print("el jugador 1 pierde")

            if z == numero_aletorio:
                print("el jugador 2 gana")
            
            if z != numero_aletorio:
                print("el jugador 2 pierde")

            if m == numero_aletorio:
                print("el jugador 3 gana")
            
            if m != numero_aletorio:
                print("el jugador 3 pierde")

            if n == numero_aletorio :
                print("el jugador 4 gana ")

            if n != numero_aletorio:
                print("el jugador 4 pierde")

            if z == numero_aletorio and x == numero_aletorio and m == numero_aletorio and n == numero_aletorio:
                print("los tres jugadores estan empatados")
#aqui se terminara toda la funcion prpia del juego pidiendo una entrada constante
    elif y == 'stop' or y == 'STOP' and y != 'start' and y != 'stop':
        break
