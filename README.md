# bliblioteca

import turtle
import time
import random

cordenada_locacion=-300

ventana=turtle.Screen()
ventana.title("YESSICA GOTIC")
ventana.setup(width= 1240, height=400)
ventana.bgcolor("grey")
ventana.tracer()

escrito=turtle.Turtle()
escrito.speed(0)
escrito.hideturtle()
escrito.penup()
escrito.goto(0,15)

cuadro = turtle.Turtle()
cuadro.speed(0)
cuadro.color("green","blue")
cuadro.begin_fill()
cuadro.hideturtle()
cuadro.penup
cuadro.goto(cordenada_locacion,0)
cuadro.pensize(5)
cuadro.pendown()
cuadro.end_fill()

numero_aletorio= random.randint(1,10)

for i in range(2):
    cuadro.forward(600)
    cuadro.left(90)
    cuadro.forward(50)
    cuadro.left(90)

escrito.write("BIENVENIDO A YESSICA GOTIC ",align="center", font=("Arial",20,'normal'))
time.sleep(2)
escrito.clear()

while True:
    y =ventana.textinput("ENTRADA ","si quieres parar escribe 'stop' \n si no escribe 'start': ")

    if y == 'start' or y == 'START':
        numero_jugadores=int(ventana.numinput("INICIO DEL JUEGO","numeros de jugadores, el numero maximo de jugadores es 4: ", minval=1, maxval=4))
        if numero_jugadores == 1:
            
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

    elif y == 'stop' or y == 'STOP' and y != 'start' and y != 'stop':
        break
