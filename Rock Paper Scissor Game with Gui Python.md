## INTRODUCTION:
This tutorial is about a game, rock paper scissors, which is used to be played peer-to-peer, but to make it on your desktop, you need a few lines of python code to pass your time.

## OUTLINE:
So in this tutorial, we will learn how to make a window-based rock paper scissors game, which can be easily understandable by the user. In this, the user plays against the computer.

## PROJECT PREREQUISITES:
tkinter: tkinter is a profound package in python. tkinter is a toolkit used in python to make graphical user interface applications. tkinter is the most commonly used and basic GUI framework used in python programming. we can easily develop window applications on our desktops by using tkinter package.

## CODE IMPLEMENTATION:

Lets get into the main code….
![](https://inprogrammer.com/wp-content/uploads/2022/07/image-147.png)
Firstly, you need to import the following packages, tkinter, and random.
These are the packages on which your entire rock paper scissors game depends on.
Now after importing these packages, you have to create a window, on which your developed game runs. **tk()** is the function from tkinter which is used to build a window.
Now we have to select the size of the window by sing the function **geometry()**. geometry is the function which is used to select the length and breadth of your window.
It depends on your interest whether to name the window or not.  If you want to name the window, **title()** is the function used to name your window.

![](https://inprogrammer.com/wp-content/uploads/2022/07/image-148.png)

Now here we defined a function named **spin()** in which we assigned values 0,1,2 to rock, paper,  scissors respectively and by using **randint()** function, we generate random value between 0,1,2 and these values were used by the computer to select its choice on a random value. Based on the choices related to the number values, it shows the concurrent result of the particular trail.

Assigning values to rock paper scissors
![](https://inprogrammer.com/wp-content/uploads/2022/07/image-149.png)

Random values by the computer and comparing them with the user’s values
![](https://inprogrammer.com/wp-content/uploads/2022/07/image-150.png)

The above part is the main part of the game on which the entire game depends on. This part is about comparing the values given by the user and the random values generated by the computer. The user can give the values by selecting the options, which can be chosen by using a dropdown box, which can be developed like this.
![](https://inprogrammer.com/wp-content/uploads/2022/07/image-151.png)

After giving user’s input,  the flow of the code enters into the spin function and then validates the result of the particular trail. For creating getting the result of the particular trail by submitting the result,  we used button to submit the result. We can create a button like this.
![](https://inprogrammer.com/wp-content/uploads/2022/07/image-152.png)

Source Code:
We are done with the code! Now let’s get a look at the entire code

``from tkinter import * 
from tkinter import ttk
from random import *
root = Tk()
root.geometry("500x500")
root.title("Rock-Paper-Scissors-Game")``

`list = ["rock","paper","scissors"]
choose_number = randint(0,2)
print(choose_number) # For testing if it works
label = Label(root,text="select your choice",width = 20,height=4,font=("calibri",15))
label.pack()
def spin():
    choose_number = randint(0,2)
    label.config(text=list[choose_number])
    if user_select.get() == "Rock":
        user_select_value = 0
        print(user_select_value)
    elif user_select.get() == "Paper":
        user_select_value = 1
        print(user_select_value)
    elif user_select.get() == "Scissors":
        user_select_value = 2
        print(user_select_value)
    if user_select_value == 0:
        if choose_number == 0:
            wl_label.config(text="Tie! - "+" Computer:Bad luck")
        elif choose_number == 1:
            wl_label.config(text="YOU Loose - "+" Computer: I am better ")
        elif choose_number == 2 :
            wl_label.config(text="YOU Won - "+" Computer: You won by luck")
    elif user_select_value == 1:
        if choose_number == 1:
            wl_label.config(text="Tie! - "+" Computer: Nice game")
        elif choose_number == 0:
            wl_label.config(text="YOU Won - "+" Computer: Shit how you are better")
        elif choose_number == 2 :
            wl_label.config(text="YOU Loose - "+" Computer: booo")
    elif user_select_value == 2:
        if choose_number == 2:
            wl_label.config(text="Tie!")
        elif choose_number == 0:
            wl_label.config(text="YOU Loose - "+" Computer: I am playing this game since i was born")
        elif choose_number == 1 :
            wl_label.config(text="YOU Won") `
            
## Adding dropdown box for Rock,Paper,Scissors
user_select = ttk.Combobox(root,value=["Rock","Paper","Scissors"])
user_select.current(0)
user_select.pack()
## Add Labels,Button
wl_label = Label(root,text="",font=("arial",10),width=50,height=4)
wl_label.pack()
button = Button(root,text="Spin",font=("bell mt",10),command=spin)
button.pack()
root.mainloop()
Output:
This is the source code. Now, let’s check by running this code.
![](https://inprogrammer.com/wp-content/uploads/2022/07/image-153.png)


So that’s it from this tutorial. Hope this project helped you in developing a window-based rock paper scissors game. You can edit the window and the inside code by having knowledge about the code and can try it yourself to your preferences.
