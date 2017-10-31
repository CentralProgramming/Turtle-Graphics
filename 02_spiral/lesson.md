# Create the Basic Spiral

```python
#import turtle module
import turtle

#make the loop that creates the spiral
for i in range(50):
  
    #move turtle forwards and turn
    turtle.forward(i*4) #set to i * any num
    turtle.right(36) #360/num of turns
```

![Basic Spiral](images/basic_spiral.png)

# Increasing Width

```python
import turtle

for i in range(50):
  
    #increase width each loop
    turtle.pensize(i)
    
    turtle.forward(i*4)
    turtle.right(36)
```

![Spiral with Changing Widths](images/width_spiral.png)

# Increasing Speed

```python
import turtle

#declare rate variable and set speed equal to it
rate = 1
turtle.speed(rate)

for i in range(50):
    
    turtle.pensize(i)
    
    #increase speed every fifth loop
    if i % 5 == 0:
        rate+=1
        turtle.speed(rate)
    
    turtle.forward(i*4)
    turtle.right(36)
```

# Alternate Colours

```python
import turtle

#create an array of colours you'd like to use
colours = ['cyan', 'blue', 'magenta', 'violet', 'skyblue']

rate = 1
turtle.speed(rate)

for i in range(50):
  
    #alternate colours
    turtle.color(colours[i % len(colours)])
    
    turtle.pensize(i)
    
    if i % 5 == 0:
        rate+=1
        turtle.speed(rate)
    
    turtle.forward(i*4)
    turtle.right(36)
```

![Colour Alternating Spiral](images/colour_spiral.png)

# Finshed Product

```python
#import turtle module
import turtle

#create an array of colours you'd like to use and set the rate
colours = ['cyan', 'blue', 'magenta', 'violet', 'skyblue']
rate = 1

#set speed to rate and hide the turtle shape 
turtle.speed(rate)
turtle.hideturtle()


#make the loop that creates the spiral
for i in range(50):
  
    #alternate colours
    turtle.color(colours[i % len(colours)])
    
    #increase width each loop
    turtle.pensize(i)
    
    #increase speed every fifth loop
    if i % 5 == 0:
        rate+=1
        turtle.speed(rate)
    
    #move turtle forwards and turn
    turtle.forward(i*4)
    turtle.right(36)
```