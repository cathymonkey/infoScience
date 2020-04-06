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

sixes = 0 ## counting


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
         
**L4**

1. What did we do?

We programmed the chessboard in the processing and made it illutional at last. Also, we made our own illutional patterns.

Here is mine:

def setup():

    size(600,400)
    background(0)
    
def draw():

    y = 25
    stroke(155)
    strokeWeight(8)
    for n in range(8):
        line(0,y,600,y)
        y += 50    
    x = 25  
      
    for n in range(12):
        line(x,0,x,400)
        x += 50 
    fill(255)
    stroke(255)   
    c = 25
    
    for m in range(12):
        p = 25
        for n in range(8):
            circle(c,p,5)
            p += 50
        c+=50
    
 
                
2. What did you learn?

I learnt how to break down a big problem into different small sections and how to create a "for loop" more complicatedly.

3.What question do I have?

Temporaily not.

**L5**

1. What did we do?

We made a short presentation of our own optical illusion that we made last class. *Note:* **one** *slide but include my 

name,my illusion and its name, the information about original illusion and its inventor, the general step to make the illusion 

and references. 

2. What did we learn?

We learnt how to demonstrate the optical illusion or work in the processing and some other information about the optical 

illusions.

3.What question do I have?

Temporarily not.

**Week 28**

1. What did we do?

I first read the article "How your personal computer can help science battle the coronavirus while you sleep" by John D'Anna
and thought about the two questions below:

*1. What are some ways in which Computer Science can help the fight against Covid-19?*

We can understand the protein structure the coronavirus contains and how these proteins work by programming a simulation on a large number of computers. Therefore, we can effectively find a treatment to stop the proteins work which means killing the virus.  

*2. In your opinion, should people enable access to the resources of their personal computers as tools for research? Are there any risks?*

I think people should but not required to. Even though the scientists have built the internet security system for the project, it can't avoid being attacked 100%. Also, there is lots of privacy in personal resources stored in the computers. However, it's really meaningful to help run the project as it can take a big step on researching coronavirus. To 
sum up, the choice is decided by people based on their trust on the project.

Then I watched the video and programmed a small part of simulation of spreading out the virus in the community.

2. What did we learn?

I learnt how to program objects moving freely within the border and here is my code:

x = [300,200,100,50,150,250,400,450,135,350,270,460,330,80]

y = [300,200,100,50,150,250,400,450,245,250,360,280,120,375]

def setup():

    size(500,500)
    
def draw():

    global x,y
    background(255)
    strokeWeight(2)
    #create individuals 
    for i in range(14):
        circle(x[i], y[i], 40) #create individual
        x[i] = x[i] + random(-10,10)
        y[i] = y[i] + random(-10,10)
        # bounderies conditions
        if x[i] > 480:
            x[i] = 480
        if x[i]< 20:
            x[i] = 20
        if y[i] >480:
            y[i] = 480
        if y[i] < 20:
            y[i] = 20    
        delay(20)

/*Q:What should be some behaviours (at least 3) that we will need to include in our simulation to be a realistic approximation of the current situation in the world? Explain./*

1) Health conditions of individuals;
2) conditions of being contracted;
3) graphs that shows the speed of spreading out the virus and the number of the infected population;
4) different population densities in different parts of the world.


3. What question do I have?

Temporaily not.

