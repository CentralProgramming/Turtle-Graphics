# Create the Basic Spiral
A spiral is made by continuously repeating a turn as if making a circle, but the length of each turn is longer than the last. This can easily be done by creating a loop, and moving to turtle an amount forwards dependent on the loop number.

## For Loops
A for loop is used to repeat code a set number of times. The general format is ` for [variable name] in range([start value], [end value], [increment])`. However, sometimes you may not need to specify a start vaule or increments if you'd like to use the defaults (0 and 1 respectively). 

The code you want to run in the loop is placed in an indented block below it. Each time the you reach the end of the loop, the counter variable is increased, beginning at the start value and stoppng right before the end value.

For example, if you wanted to print all the numbers from 1-10, it you could do so with the following loop:
```pyhon
for i in range(10):
  print(i+1)
```
Since `i` starts at 0 and ends at 9, you have to add 1 to `i` before printing it. Alternatively, you could write the loop like this:
```pyhon
for i in range(1,11):
  print(i)
```

## Code
```python
#import turtle module
import turtle

#make the loop that creates the spiral
for i in range(50): #50=num turns, can be any number
  
    #move turtle forwards and turn
    turtle.forward(i*4) #set to i * any num
    turtle.right(36) #360/num of turns
```

<img src="images/base_spiral.png" alt="Basic Spiral" width="500" height="477">


# Increasing Width

```python
import turtle

for i in range(50):
  
    #increase width each loop
    turtle.pensize(i)
    
    turtle.forward(i*4)
    turtle.right(36)
```

<img src="images/width_spiral.png" alt="Spiral with Changing Widths" width="500" height="477">


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

<img src="images/colour_spiral.png" alt="Colour Alternating Spiral" width="500" height="477">


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