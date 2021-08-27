# CONTADORES-MAQUINAS
CREAR UN FORMULARIO DONDE INGRESO CONTDORES, DIARIOS DE MAQUINAS ELECTRONICAS QUE AUMENTAN ENTRADA DIARIAS Y SALIDAS DIARIAS
#Código del programa maquinas CONTADORES
from tkinter import Tk,Text,Button,END,re

class Interfaz:
    def __init__(self, ventana):
        #Inicializar la ventana con un título
        self.ventana=ventana
        self.ventana.title("Contadores")


        #Agregar una caja de texto para que sea la pantalla de la calculadora
        self.pantalla=Text(self.ventana, state="disabled", width=40, height=3, background="orchid", foreground="white", font=("Helvetica",15))

        #Ubicar la pantalla en la ventana
        self.pantalla.grid(row=0, column=0, columnspan=4, padx=5, pady=5)

        #Inicializar la operación mostrada en pantalla como string vacío
        self.operacion=""
 
        # crear cada maquina
        boton1=self.crearBoton(1)
        boton2=self.crearBoton(2)
        boton3=self.crearBoton(3)
        boton4=self.crearBoton(4)
        boton5=self.crearBoton(5)
        boton6=self.crearBoton(6)
        boton7=self.crearBoton(7)
        boton8=self.crearBoton(8)
        boton9=self.crearBoton(9)
        boton10=self.crearBoton(10)
        boton11=self.crearBoton(11)
        boton12=self.crearBoton(12)
        boton13=self.crearBoton(13)
        boton14=self.crearBoton(14)
        boton15=self.crearBoton(15)
        boton16=self.crearBoton(16)
        boton17=self.crearBoton(17)
        boton18=self.crearBoton(18)
        boton19=self.crearBoton(19)
        boton20=self.crearBoton(20)
         #Ubicar los botones con el gestor grid
        maquina=[boton1, boton2, boton3, boton4, boton5, boton6, boton7, boton8, boton9, boton10, boton11, boton12, boton13, boton14, boton15, boton16, boton17, boton18, boton19, boton20]
        contador=0
        for fila in range(1,6):
            for columna in range(4):
                maquina[contador].grid(row=fila,column=columna)
                contador+=1
        return


    #Crea un botón mostrando el valor pasado por parámetro
    def crearBoton(self, valor, escribir=True, ancho=9, alto=1):
        return Button(self.ventana, text=valor, width=ancho, height=alto, font=("Helvetica",15), command=lambda:self.click(valor,escribir))

        


ventana_principal=Tk()
Contadores=Interfaz(ventana_principal)
ventana_principal.mainloop()
