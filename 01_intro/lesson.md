# Introduction
Imagine that there's a turtle holding a pen on a canvas. The turtle controls the pen, creating a line with it wherever it moves. It can go forwards or backwards according to its heading, or the angle in which it is facing. This is the concept behind turtle graphics. By controlling the "turtle" (which looks like an arrow by default), you can create lines, shapes, and other images.

##  Setting Up
Before we can get started, we'll have to import the turtle module.
```python
import turtle
```
>If you'd like to use a short form, you can use `import turtle as t` and then write `t` instead of `turtle` in commands (`turtle.forwards(10)` would become `t.forwards(10)`)

# Moving the Turtle
___

## Forwards
To move the turtle forwards in the direction it is facing, use:
```python
turtle.forward(distance)
turtle.fd(distance) #short form
```
For example, if you want to move the turtle forward 100 units, you would write `turtle.forward(100)`.

![Forward Line](images/forward_line.png =133x40)

## Backwards
Moving backwards from the direction it is facing uses the same principle.
```python
turtle.backward(distance)
turtle.bk(distance) #short form
```

# Rotating the Turtle
___
So the turtle can move forwards and backwards. That's great, but we can't really draw much with a line in only one direction. The turtle can either be rotated relative to its current heading (left or right), or set absolutly. The initial heading of the turtle is 0 (right)

## Rotate Left
```python
turtle.left(degrees)
turtle.lt(degrees)  #short form
```

## Rotate Right
```python
turtle.right(degrees)
turtle.rt(degrees)  #short form
```

## Set Absolute Heading
```python
turtle.setheading(degrees)
turtle.seth(degrees)  #short form
```

## Relative vs. Absolute
If the turtle is facing 180 degrees currently (left/west), and you were to move it 90 degrees left, it would now be facing down at 270 degrees. However, if you set its absolute heading to 90 degrees, it would now be facing up, regardless of where it started.

![Directions & Corresponding Degrees](images/directions.png =250x250)

# Testing it Out
___
Now that you know the basics, let's put it into practice.

Try making a square by repeativly moving forwards and turning the turtle at a right angle. For a challenge, try making it in a loop, or creating a function that will create squares of different sizes.

The result should look something like this:

![Basic Square](images/basic_square.png =146x135)