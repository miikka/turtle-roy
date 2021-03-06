# Turtle Roy

A [Roy](http://roy.brianmckenna.org/) programming/learning environment with [Turtle Graphics](http://en.wikipedia.org/wiki/Turtle_graphics), as in the
[Logo](http://el.media.mit.edu/logo-foundation/logo/programming.html) programming language.

Try it online: [turtle-roy.heroku.com/](http://turtle-roy.heroku.com/)

# Turtle Roy API

    fd x    | moves x pixels forward
    lt x    | turns left x degrees
    rt x    | turns right x degrees
    penup   | lifts the pen, no trace left when moving
    pendown | lowers the pen again for drawing
    clear   | clear the paper and reset turtle to center

# Examples

Bunch of examples available in the demo menu. Some more stuff here.

Basic Turtle commands

    fd 100
    lt 90
    rt 45

Square

    let square = repeat 4 (sequence[fd 50, lt 90])
    square

Flower

    let flower = repeat 36 (rt 10, square)
    flower

Math

    3 + 4
    3 / 4
    let factorial n = if n==1 then 1 else n * (factorial n - 1)
    factorial 12

Strings

    "apple" ++ "sauce"
    "apple" + 10 (won't compile)

Lists

    range 1 99
    head [1,2,3]
    tail [1,2,3]
    concat [1,2,3] [4,5,6]
    length [1,2,3]
    let reverse xs = if (empty xs) then [] else concat (reverse (tail xs)) [head xs]
    reverse [1,2,3]
    
# Running

    ./sbt ~container:start

# Credits

Thanks to Miikka "arcatan" Koskinen for creating [tryroy](https://github.com/miikka/tryroy), from where I shamelessly stole the Roy browser REPL.

Thanks to Brian McKenna for the [Roy](https://github.com/pufuwozu/roy) language and support.
