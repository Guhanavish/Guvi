# Guvi
Project
from tkinter import *
from math import *

#Creating the main window
root = Tk()
root.title("Scientific GUI Calculator")

#Creating the display frame
displayFrame = Frame(root)
displayFrame.pack(side = TOP, expand = YES, fill = BOTH)

#Creating the display
display = Entry(displayFrame, font = ("arial", 20, "bold"), bd = 30, width = 28, bg = "powder blue", justify = RIGHT)
display.pack(side = TOP, expand = YES, fill = BOTH)

#Creating the buttons frame
buttonsFrame = Frame(root)
buttonsFrame.pack(side = TOP, expand = YES, fill = BOTH)

#Creating the first row of buttons
button1 = Button(buttonsFrame, text = "sinh", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("sinh"))
button1.grid(row = 0, column = 0)

button2 = Button(buttonsFrame, text = "cosh", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("cosh"))
button2.grid(row = 0, column = 1)

button3 = Button(buttonsFrame, text = "tanh", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("tanh"))
button3.grid(row = 0, column = 2)

button4 = Button(buttonsFrame, text = "sin", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("sin"))
button4.grid(row = 0, column = 3)

#Creating the second row of buttons
button5 = Button(buttonsFrame, text = "cos", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("cos"))
button5.grid(row = 1, column = 0)

button6 = Button(buttonsFrame, text = "tan", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("tan"))
button6.grid(row = 1, column = 1)

button7 = Button(buttonsFrame, text = "log", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("log"))
button7.grid(row = 1, column = 2)

button8 = Button(buttonsFrame, text = "ln", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("ln"))
button8.grid(row = 1, column = 3)

#Creating the third row of buttons
button9 = Button(buttonsFrame, text = "sqrt", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("sqrt"))
button9.grid(row = 2, column = 0)

button10 = Button(buttonsFrame, text = "1/x", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("1/x"))
button10.grid(row = 2, column = 1)

button11 = Button(buttonsFrame, text = "x^2", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("x^2"))
button11.grid(row = 2, column = 2)

button12 = Button(buttonsFrame, text = "x^y", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("x^y"))
button12.grid(row = 2, column = 3)

#Creating the fourth row of buttons
button13 = Button(buttonsFrame, text = "+", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("+"))
button13.grid(row = 3, column = 0)

button14 = Button(buttonsFrame, text = "-", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("-"))
button14.grid(row = 3, column = 1)

button15 = Button(buttonsFrame, text = "*", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("*"))
button15.grid(row = 3, column = 2)

button16 = Button(buttonsFrame, text = "/", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("/"))
button16.grid(row = 3, column = 3)

#Creating the fifth row of buttons
button17 = Button(buttonsFrame, text = "=", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("="))
button17.grid(row = 4, column = 0, columnspan = 2)

button18 = Button(buttonsFrame, text = "C", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("C"))
button18.grid(row = 4, column = 2)

button19 = Button(buttonsFrame, text = ".", font = ("arial", 20, "bold"), bd = 10, padx = 10, pady = 10,
command = lambda: button_click("."))
button19.grid(row = 4, column = 3)

#Function to manage the clicks
def button_click(key):
    if key == "=":
        result = str(eval(display.get()))
        display.delete(0, END)
        display.insert(END, result)
    elif key == "C":
        display.delete(0, END)
    elif key == "sinh":
        result = str(sinh(float(display.get())))
        display.delete(0, END)
        display.insert(END, result)
    elif key == "cosh":
        result = str(cosh(float(display.get())))
        display.delete(0, END)
        display.insert(END, result)
    elif key == "tanh":
        result = str(tanh(float(display.get())))
        display.delete(0, END)
        display.insert(END, result)
    elif key == "sin":
        result = str(sin(float(display.get())))
        display.delete(0, END)
        display.insert(END, result)
    elif key == "cos":
        result = str(cos(float(display.get())))
        display.delete(0, END)
        display.insert(END, result)
    elif key == "tan":
        result = str(tan(float(display.get())))
        display.delete(0, END)
        display.insert(END, result)
    elif key == "log":
        result = str(log(float(display.get())))
        display.delete(0, END)
        display.insert(END, result)
    elif key == "ln":
        result = str(log1p(float(display.get())))
        display.delete(0, END)
        display.insert(END, result)
    elif key == "sqrt":
        result = str(sqrt(float(display.get())))
        display.delete(0, END)
        display.insert(END, result)
    elif key == "1/x":
        result = str(1 / float(display.get()))
        display.delete(0, END)
        display.insert(END, result)
    elif key == "x^2":
        result = str(float(display.get()) ** 2)
        display.delete(0, END)
        display.insert(END, result)
    elif key == "x^y":
        result = str(float(display.get()) ** float(display.get()))
        display.delete(0, END)
        display.insert(END, result)
    else:
        display.insert(END, key)

#Running the main loop
root.mainloop()
