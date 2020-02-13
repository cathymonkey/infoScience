# This is the journal for Comp Sci
**L1**

1. What did we do?

  We watched the video of the introduction to computer science and learnt about four main elements of computational thinking.   Then we wrote the detailed procedures of making a jam sandwich.
  
2. What did you learn?

  I learnt how precisely and specifically we need to do something in a logical way.  
  
3. What question do I have?

  
  Temporarily none.
  
**L2**

1. What did we do?

We programmed a normal dice and a biased dice in the processing. We also guessed each other's biased number of the biased dice.

2. What did you learn?

I had a lot of fun while learning how to program a biased dice in the processing and guessed the biased number based on the probability.

3. What question do I have?

Temporarily none.

**L3**

1. What did we do?

We continued programming the dice in the processing and drew the graph to help us observe.

ones = 0
twos = 0
threes = 0
fours = 0
fives = 0
sixes = 0## counting

def setup():
    size(600,800)

def draw():
    x=0
    delay(200)
    mouseClick()
    barGraph()
    
def barGraph():
    global ones
    fill(0)
    textSize(20)
    for x in range(6):
        text(x+1,(50+50*x),580)
    fill(255,0,0)    
    rect(50,550-ones, 20, ones)
    rect(100, 550-twos, 20, twos)
    rect(150, 550-threes, 20, threes)
    rect(200, 550-fours, 20, fours)
    rect(250, 550-fives, 20, fives)
    rect(300, 550-sixes,20, sixes)

    
    
    
def mouseClick():
    global ones, twos, threes, fours, fives, sixes
    background(255)
    stroke(0)
    fill(255)
    strokeWeight(5)
    rect(100,100,400,400,10)
    stroke(255,0,0)
    n = random(0,3.0)
    if 0<=n<0.5:
        circle(300,300,50)
        ones += 1
        print("Number of times one has been rolled:",ones)
    
    if 0.5<=n<1.1:
        circle(200,200,50)
        circle(400,400,50)
        twos += 1
        
    if 1.1<=n<1.6:
         circle(200,200,50)
         circle(400,400,50)         
         circle(300,300,50)
         threes += 1
    if 1.6<=n<2.1:
         circle(200,200,50)
         circle(400,400,50)
         circle(200,400,50)
         circle(400,200,50)
         fours += 1
         
    if 2.1<=n<2.5:
         circle(200,200,50)
         circle(400,400,50)
         circle(200,400,50)
         circle(400,200,50)
         circle(300,300,50)
         fives += 1
         
    if 2.5<=n<3.0:
         circle(200,200,50)
         circle(400,400,50)
         circle(200,400,50)
         circle(400,200,50)
         circle(200,300,50)
         circle(400,300,50)
         sixes += 1 
          
2. What did you learn?

I learnt how to draw a bargraph to record the counting.

3. What question do I have?

If I want to choose Computer Science in G11, what should I prepare?
         
            


