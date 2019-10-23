# Games Programming



[https://www.sqa.org.uk/files/nu/FN8R11.pdf](https://www.sqa.org.uk/files/nu/FN8R11.pdf)

Upon Completion of this Unit you will be able to

* Design a game concept
* Produce a Working Demo
* Evaluate Demo

{% file src="../../.gitbook/assets/task-sheet.docx" caption="Task Sheet" %}

Commenting Indentation Naming Variables Data Structures Control Structures Operators

## Pico-8

[https://www.lexaloffle.com/pico-8.php](https://www.lexaloffle.com/pico-8.php)

Pico-8 is an IDE \( Integrated Developer Environment \) that uses the Lua programming language.

Pico-8 attempts to replicate the limitations of 8bit video games systems.

Sticking to these limitations helps us to control the scope of our projects and means we only have to worry about one program when we are starting out.

![enter image description here](https://www.lexaloffle.com/gfx/p8_jelpi.gif)

Text Commands Code Editor Sprite Editor Tile Editor Sound Effects Music Tracker

init draw update

## Making your first game

We press Escape to enter the blank code screen In order to clear the screen we type;

```text
CLS()
```

If we run this code we can see that the screen is cleared

 Next we can type;

```text
PRINT("HELLO")
```

This will print the word hello on the screen.

 If we want to draw a sprite on screen we will type;

```text
SPR(0,64,64)
```

In this example 0 selects sprite slot 0, 64 draw the sprite 64 pixels along horizontally, and, the next 64 draws the sprite 64 pixels along vertically

 In order to make our sprite move horizontally, we need to perform arithmetic on the first 64. To do this, we need to substitute 64 with a value - for example x. We will need to define what x is, now we can perform arithmetic on the value x.

```text
SPR(0,x,64)
X=64
X=X+1
```

 At this point we need to split our code into the three built-in functions used in pico-8.

**FUNCTION \_INIT\(\)** This function contains and initializes all the variables that we will use.

**FUNCTION \_DRAW\(\)** This function describes all the elements that will be drawn on the screen.

**FUNCTION \_UPDATE\(\)** This function contains all of the game logic. This function is called 30 times each second.

```text
FUNCTION _INIT()
    x=64
END

FUNCTION _DRAW()
    SPR(0,x,64)
END

FUNCTION _UPDATE()
    X=X+1
END
```

This example will sho our sprite moving to the right forever.

 Now we want to move the sprite only when we press a key.

```text
FUNCTION _UPDATE()
    IF BTN(1) THEN
        X=X+1
    END
END
```

Now our sprite will only move when we press the right arrow key.

 In order to make the sprite move in two directions, we can reuse our code and change the name of the button used, as well as the arithmetic.

```text
    FUNCTION _UPDATE()
         IF BTN(1)
             THEN X=X+1
         END

           IF BTN(0)
             THEN X=X-1
         END
    END
```

Now our sprite can move both to the left and to the right.

 As it stand right not, our sprite can move off of the screen - in order to stop this we can set some limits.

```text
FUNCTION _UPDATE()
    IF BTN(1) THEN
        X=X+1
    END

    IF BTN(0)THEN
         X=X-1
    END

    IF X>120 THEN
        X=120
    END

END
```

We can use this to limit the movement in the other direction as well.

```text
FUNCTION _UPDATE()
    IF BTN(1) THEN
        X=X+1
    END

    IF BTN(0)THEN
         X=X-1
    END

    IF X>120 THEN
        X=120
    END

    IF X<0 THEN
        X=0
    END

END
```

 In order to animate the sprite, we need to manipulate the sprite value. First we need to substitute 0 for S in our draw function, then we can add S=0 in our init function, then we can apply arithmetic and limits in our update function.

You should always avoid using sprite slot 0.

```text
 FUNCTION _INIT()
    X=64
    S=1
 END

 FUNCTION _DRAW()
      CLS()
    SPR(S,X,64)
 END

 FUNCTION _UPDATE()
   IF BTN(1) THEN
    X=X+1
     END

    IF BTN(0)THEN
    X=X-1
    S=S+1
    END

    IF X>120 THEN
    X=120
    END

    IF X<0 THEN
    X=0
    END

    IF S>2 THEN
    S=1
    END

END
```

 In order to flip our sprite horizontally, we can add additional information to our sprite line.

```text
SPR(S,X,64,1,1,TRUE)
```

In order to manipulate this value 'TRUE', we need to give it a name and then initialize it in our init function.

```text
SPR(S,X,64,1,1,F)
```

```text
F=FALSE
```

```text
   FUNCTION _INIT()
    X=64
    S=1
    F=FALSE
 END

 FUNCTION _DRAW()
      CLS()
    SPR(S,X,64)
 END

 FUNCTION _UPDATE()
   IF BTN(1) THEN
    X=X+1
    S=S+1
    F=FALSE
    END


    IF BTN(0)THEN
    X=X-1
    S=S+1
    F=TRUE
    END

    IF X>120 THEN
    X=120
    END

    IF X<0 THEN
    X=0
    END

    IF S>2 THEN
    S=1
    END

END
```

Now our sprite will flip direction depending on which way it is travelling.

 At this point our code is becoming difficult to read, so we should add comments.

```text
FUNCTION _INIT()
    X=64--HORIZONTAL SPRITE VALUE
    S=1--SPRITE SLOT
    F=FALSE--FLIP SPRITE HORIZONTALLY
END

FUNCTION _DRAW()
     CLS()--CLEAR SCREEN
    SPR(S,X,64)--DRAW SPRITE
END

FUNCTION _UPDATE()
    IF BTN(1) THEN--RIGHT KEY
    X=X+1--MOVE SPRITE RIGHT
    S=S+1--ANIMATE
    F=FALSE
    END


    IF BTN(0)THEN--LEFT KEY
    X=X-1--MOVE SPRITE LEFT
    S=S+1--ANIMATE
    F=TRUE--FLIP SPRITE
    END

    IF X>120 THEN--LIMIT X AT RIGHT EDGE OF SCREEN
    X=120
    END

    IF X<0 THEN--LIMIT X AT LEFT EDGE OF SCREEN
    X=0
    END

    IF S>2 THEN--LOOP ANIMATION
    S=1
    END

END
```

