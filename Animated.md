import tkinter as tk

def move_rectangle():
    canvas.move(rectangle, 1, 0)
    root.after(10, move_rectangle)  # Move every 10 milliseconds

root = tk.Tk()
root.title("Simple Animation")

canvas = tk.Canvas(root, width=200, height=100)
canvas.pack()

rectangle = canvas.create_rectangle(10, 10, 30, 30, fill="blue")

move_rectangle()  # Start the animation

root.mainloop()
import tkinter as tk

def move_circle(dx, dy):
    canvas.move(circle, dx, dy)
    root.after(10, move_circle, dx, dy)  # Move every 10 milliseconds

root = tk.Tk()
root.title("Simple Circular Animation")

canvas = tk.Canvas(root, width=200, height=200)
canvas.pack()

circle = canvas.create_oval(50, 50, 100, 100, fill="red")

# Initial direction of movement
dx = 1
dy = 1

# Start the animation
move_circle(dx, dy)

root.mainloop()
