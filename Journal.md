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

**1. What did we do?**

I first read the article "How your personal computer can help science battle the coronavirus while you sleep" by John D'Anna
and thought about the two questions below:

*1. What are some ways in which Computer Science can help the fight against Covid-19?*

We can understand the protein structure the coronavirus contains and how these proteins work by programming a simulation on a large number of computers. Therefore, we can effectively find a treatment to stop the proteins work which means killing the virus.  

*2. In your opinion, should people enable access to the resources of their personal computers as tools for research? Are there any risks?*

I think people should but not required to. Even though the scientists have built the internet security system for the project, it can't avoid being attacked 100%. Also, there is lots of privacy in personal resources stored in the computers. However, it's really meaningful to help run the project as it can take a big step on researching coronavirus. To 
sum up, the choice is decided by people based on their trust on the project.

Then I watched the video and programmed a small part of simulation of spreading out the virus in the community.

**2. What did we learn?**

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

*Q:What should be some behaviours (at least 3) that we will need to include in our simulation to be a realistic approximation of the current situation in the world? Explain.*

1 Health conditions of individuals; - we can use different colors to represent the person is healthy or infected

2 conditions of being contracted;- we can assume if an infected person met with another person in a room for a certain time or for many times, then another person is going to be infected

3 graphs that shows the speed of spreading out the virus and the number of the infected population;- program graphs

4 different population densities in different parts of the world - program different number of individuals in different areas.


**3. What question do I have?**

Temporaily not.

**Week 29**

**1. What did we do?**

We first worked on some small programs as the following:

def printBears():


  for i in range(0, 101, 1):
  
    if i == 1:
    
      print(i, "bear")
    else:
      print(i, "bears")

def printYears():

    for i in range(1900, 2001, 1):
        print("The year is", i)
        
def temperature():

    for i in range(0, 101, 1):
        f = round(i*1.8 + 32,2) # remain two decimals
        print(i, "C are", f, "F")
        
printBears()

printYears()

temperature() 

Then we kept working on the simulation of spreading out the coronavirus. We drew the bargraphs and counted the number of iterations until all the population is infected. 

x = [100,200]

y = [100,250]

h = [False, True]

healthy =0

infected = 0

iteration = 0

def setup():

    size(500,500)
    for i in range(23):
        x.append(random(0,500))
        y.append(random(0,500))
        h.append(True)#healthy
        
def distance(x1, x2, y1, y2):

    a = (x1-x2)
    b = (y1-y2)
    c = sqrt(a**2+b**2)
    return c 

def draw():

    global x,y,healthy,infected,iteration
    background(255)
    bargraph()
    for ind in range(len(x)):
        if h[ind] == True:
            fill(0,255,0)# green healthy
        
            
            
        else:
            fill(255,0,0)# red infected
        
        
        circle(x[ind],y[ind],40)
        #calculate the distance to each neighbour
        for nei in range(len(x)):
            if nei == ind:
                continue
                
            
            d = distance(x[ind],x[nei], y[ind], y[nei])
            if d <= 40 and (h[nei] == False or h[ind] == False):
                h[ind] = False
                h[nei] = False
        
    #move the individuals
    for m in range(len(x)):
        iteration += 1
        print("iteration",iteration)
        x[m] += random(-20,20)
        y[m] += random(-20,20)
        
        if x[m] > 480: x[m] = 480
        if x[m] < 20: x[m] = 20
        if y[m] < 20: y[m] = 20
        if y[m] > 480: y[m] = 480
        
    delay(100)
    # number of healthy/sick
    infected=0
    healthy=0
    for n in range(len(h)):
        if h[n] == False:
            infected +=1
        else:
            healthy += 1
    # here increase iterations
    iteration += 1     
        
def bargraph():

    fill(0)
    textSize(12)
    text("infected",10,450)
    text(infected, 40+infected+50, 460)
    text("healthy", 10,480)
    text(healthy,40+healthy+50,490)
    text("iteration:",380,470)
    text(iteration, 440,470) 
    fill(255,0,0)
    rect(40, 450, 40+infected, 10)
    fill(0,255,0)
    rect(40, 480, 40+healthy, 10)
        
        
 Also, we filled in the table below to find out some relations between different factors when the virus is spreading.
 
 *Relations between the number of people moving and its infecting speed* 
 
 Case Number  |    Number of people moving  |   Population size    |   Number of iterations until all population is infected
 
      1             25                        25                        11411

      2             20                        25                        7244
      
      3             15                        25                        6095
      
      4             10                        25                        8840
      
      5             5                         25                        8549
      
  Conclusion: Usually, the more people are moving, the longer time it will take to infect the whole population. Sometimes,
  however, if there are only a few people are moivng, it will take them more time to infect the virus to the whole population.
  
  Here is another table to show the relation between population size in a certain area and the infecting speed.
  
  *Relations between the number of people moving and its infecting speed
  
   Case Number  |    Number of people moving  |   Population size    |   Number of iterations until all population is infected
  					
     1				25			25				6577																		
     2		                40			40				5411													
     3				50			50				5252

     4				80			80				4616
    
     5				100			100				4746
			
Conclusion: According to the calculations, the speed of infecting each indidual is faster when there are more people
in a certain area. So, virus can spread out in a more densed place and that's why recently we avoid going to public
places and gatherings where has the highest risk of being infected.

**2. What did we learn?**

I learnt how to make a counter in Python and understood the important factors we should consider when making a simulaiton. By 
making this simulation, I mastered some new skills and drew some conclusions to help us protect ourselves during the coronavirus period. I enjoyed this task.

**3. What questions do I have?**

Temproraily not.

**Week 31**

1. What did we do?

I kept doing the simulation of how coronavirus spread and added how people would be treated. After finishing the simulation, I 

did a reflection video on the simulation project.

x = [100,200]

y = [200,100]

h = ["healthy", "infected"]

healthy = 0

infected = 2

recovered = 0

peopleMoving = 30

iteration = 0

days = [30,-1]

rDays = int(random(30,60))


def setup():

    global x,y,h,peopleMoving
    size(500,600)
    for i in range(28):           
        x.append(random(0,500))
        y.append(random(0,500))
        h.append("healthy")
        days.append(-1)
        
def distance(x1, x2, y1, y2):

    a = (x1-x2)
    b = (y1-y2)
    c = sqrt(a**2+b**2)
    return c 

def draw():

    global x,y,healthy,infected,iteration,recovered,peopleMoving,days,rDays
    background(255)
    bargraph()

    for ind in range(peopleMoving):
        if h[ind] == "healthy":
            fill(0,255,0)# green healthy
            
        elif h[ind] == "recovered": # blue recovered
            fill(0,250,255)
            
        else:
            fill(255,0,0)  # red infected
            
        if h[ind] == "infected":
            days[ind] -= 1
            if days[ind] == 0:
                h[ind] = "recovered"
                recovered += 1
                days[ind] = 0   
        
        circle(x[ind],y[ind],40)
        #calculate the distance to each neighbour
        for nei in range(peopleMoving):
            if nei == ind:
                continue
                
            
            d = distance(x[ind],x[nei], y[ind], y[nei])
            if d <= 40 and (h[nei] == "infected" or h[ind] == "infected"):
                if h[nei] == "healthy":
                    h[nei] = "infected"
                    days[nei] = rDays
                if h[ind] == "healthy":
                    h[ind] = "infected"
                    days[ind] = rDays
             
    
        
    #move the individuals
    for m in range(peopleMoving):
        iteration += 1
        print("iteration",iteration)
        x[m] += random(-20,20)
        y[m] += random(-20,20)
        
        if x[m] > 480: x[m] = 480
        if x[m] < 20: x[m] = 20
        if y[m] < 20: y[m] = 20
        if y[m] > 480: y[m] = 480
        
    delay(100)
    # number of healthy/sick
    infected=0
    healthy=0
    recovered=0
    for n in range(len(h)):
        if h[n] == "infected":
            infected +=1
        elif h[n] == "recovered":
            recovered += 1
        else:
            healthy += 1
    # here increase iterations
    iteration += 1
        
        
def bargraph():

    peopleMoving = len(x)
    line(0,500,500,500)
    fill(0)
    textSize(14)
    text("peopleMoving:",360,550)
    text(peopleMoving,470,550)
    text("recovered",10, 520)
    text(recovered, 40+recovered+50,515)
    text("infected",10,550)
    text(infected, 40+infected+50, 540)
    text("healthy", 10,580)
    text(healthy,40+healthy+50,570)
    text("iteration:",360,570)
    text(iteration, 430,570) 
    fill(255,0,0)
    rect(90, 540, infected, 13)
    fill(0,255,0)
    rect(90, 570, healthy, 13)
    fill(0,250,255)
    rect(90,510,recovered,13)
        

2. What did we learn?

I learnt how important and helpful roles computer science plays in our daily life. Also, I learnt how to program the counter 

and set mutiple conditions. 

3. What questions do I have?

Temproraily not.

**Week 33 - Cryptography**

I really like cryptography.

1. What did we do?

We deciphered the texts by using Caesar Cipher(letter frequency).

This is the first original text:"F gtd bfx fy f hfwsnafq fsi bjsy yt f gttym bmjwj f rfs xfni yt ymj gtd, "Nk N bwnyj dtzw 

jcfhy

bjnlmy ts ymnx unjhj tk ufujw ymjs dtz mfaj yt lnaj rj $50, gzy nk N hfssty, N bnqq ufd dtz $50." Ymj gtd qttpji fwtzsi fsi

xfb st xhfqj xt mj flwjjx, ymnspnsl st rfyyjw bmfy ymj hfwsd bwnyjx mj'qq ozxy xfd mj bjnlmx rtwj tw qjxx. Ns ymj jsi ymj gtd 

jsiji zu ufdnsl ymj rfs $50. Mtb ini ymj rfs bns ymj gjy?"


Decode: A boy was at a carnival and went to a booth where a man said to the boy,"If I write your exact weight on this piece of 

paper then you have to give me $50, but if I cannot, I will pay you $50." The boy looked around and saw no scale so he agrees, 

thinking no matter what the carny writes he'll just say he weighs more or less. In the end the boy ended up paying the man 

$50. How did the man win the bet? 

Answer: Because the man wrote "your exact weight" on the paper.

Then I watched the video about Cicada 3310 which was an internet mystery.

What were the clues used in the cicada scavenger hunt?

They were the encrypted web address after extracting an image or encrypted books or audio.

2. What did we learn?

We learnt one of the ways to deciphering the code( Caesar Cipher) and leanrt about an interesting mystery about cryptography.

3. What questions do I have?

How can we encrypt the symbols and numbers? Also, I think leaving space between words and words will make it easier to decode.

For the first one, I simply thought "A" is usually put in the beginning of the sentence as a word, so I only tried one time 

and it was decoded. 

