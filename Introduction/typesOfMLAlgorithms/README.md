[Previous Chapter: Introduction](https://github.com/pbharathreddy/Machine-Learning/blob/master/README.md)

# Types of Machine Learning Algorithms
There are mainly **3** types of algorithms a machine learning model can be trained:
1. Supervised 
1. Unsupervised
1. Reinforcement

Let’s take an example to understand these terms:

Think about the time when you were a school kid, try to recreate the picture of your typical Math classroom. Even today, I get freaked out to imagine my teacher calling me to solve an example on the blackboard in front of my class! 
So, the problem which you are going to solve on the board might be of the following type:
* Your teacher has solved a problem on the blackboard and has asked you to solve a **similar** one! Hmm, not bad actually. This teacher of yours sounds really good!
* Your teacher has just written a problem and the solution is, well, you have to find out by **yourself**, the only hint is more amount of similar kind of problems given. Your task is to figure out the pattern in those problems and to come up with a solution. Sounds like fun and challenging, this teacher has their own way of teaching!
* Your teacher calls you to solve a problem **without** giving you any hint, you just have to start solving it, they will give you a chocolate if you going on a right track  or else they will give you an extra assignment as a punishment, so you have to figure out how to get more chocolates and fewer assignments as possible, i.e which similar kind of steps to repeat to get a **reward**, this sounds the hardest, your teacher is simply a legend!!

## 1. Supervised learning:
Supervised learning is the first type of problem discussed above. When a model is trained with **features** (problem statement in our example) **along** with the **labels** (solutions of the problem), it is known as supervised learning. It is used to solve types of problems like **classification and regression**.
A classification problem is when our y, the output variable, the dependent variable or any name which you like the best, is a **categorical** variable and using the features you have to predict the label belonging to one class or the other, while a **regression** problem is when the label is a continuous value and not belonging to a certain class, having a big possibility of values. More on that later.


<p align="center">
<img width=300 src="../../images/spoon-feeding.jpg" alt="Spoon-feeding image" />
</p>
Enough of spoon-feeding! Now let’s get unsupervised!

## 2. Unsupervised learning:
The second type is unsupervised learning. When we **only** have features and not labels for training, it is called unsupervised. It can be used to solve the following types of problems:
* Clustering
* Dimensionality Reduction

### Clustering:
Clustering means categorizing the data points (i.e each row, observation, etc) into a group. Note that we don’t categorize them based on given parameters or labels but it tries to figure out on its own, that’s why it is an unsupervised algorithm. Let’s learn the concept of clustering with a simple example. Imagine that a 3-year-old is given a deck of cards and is given a task to group the cards the way he or she likes. The child starts searching for patterns and sees that each card has either a number or a picture (joker, jack, queen, king, A), a symbol (i.e. spade, ace, heart, and diamond), and color. So there are many possibilities based on which the deck can be divided. He or she is not instructed about how to divide or in how many groups, so that is unsupervised and thus it depends on the child to divide it into 2 groups (based on a number card and picture card, red and black color cards), 4 groups (based on the symbol), or simply 1! If they believe in this:

<p align="center">
<img width=500 src="../../images/clustering.jpg" alt="There are two types of people, those who divide others in 2 types and those who don't"/>
</p>

In short, what the child did in our case is called clustering, more on that later.

### Dimensionality Reduction:
Dimensionality Reduction means, getting only those **columns/features** which are relevant to our problem and omitting other columns to reduce the complexity of the data. For example, let’s say our task is to predict from a given data of wizards and witches (yes, I am a potterhead!), which ones will go bad in the future. The data given has features / columns like Name, Hogwarts House (That might be the major feature to decide), Height, Weight, Favourite subject, Family, i.e. Muggle born or from a wizard family, and their Boggart (meaning, from what are they afraid of). 


ID | Name | Hogwarts House | Height | Weight | Favourite subject | Blood Status | Boggart 
--- | --- | --- | --- | --- | ---  | --- | --- 
| 1 | Tom Riddle | Slytherin | 5’11’’ | 50 | Dark Arts | Half Blood | His own Corpse |
| 2 | Harry Potter | Gryffindor | 5’8’’ | 65 | Defense against dark arts | Half Blood | Dementor |
| 3 | Albus Dumbledore | Gryffindor | 5’11’’ | 70 | Transfigurations | Half Blood | Corpse of his sister |
| 4 | Hermione Granger | Gryffindor | 5’4’’ | 60 | Charms | Muggle | Failure | 
| 5 | Ronald Weasley | Gryffindor | 5’11’’ | 68 | Chess | Pure Blood | Spider | 
| 6 | Draco Malfoy | Slytherin | 5’9’’ | 67 | Dark Arts | Pure Blood | Lord Voldemort |


*(Huffulpuff and Ravenclaw people (BTW I am a Ravenclaw as well!), don't get upset if you don't find your house name in this list, because to check if a wizard is good or bad, when it comes to the later groups, records say it has never happened! So, no need to check, cheers!!)*

Here note that some of the features are not useful to predict the outcome, like the height and the weight, i.e. the appearance of the person does not decide whether they are a good person or bad (but in movies, they do!), so we can drop those columns. This decreases the complexity of our data and that way, we can focus on our problem easily. We can divide the process of reduction into 2 parts:
1. Feature Selection
1. Feature Extraction

We will discuss these phases and the methods in detail in later chapters.

## 3. Reinforcement Learning:
As shown in the third example, this method is useful of stochastic environment, which are applicable for real world problems, where there are so much uncertainities and dynamically the decision has to be taken and whether the step taken was a positive or rewarding or negative can only be determined after taking that step and the next step should be taken after considering previously taken steps and figuring out patterns out of the historic data. The best example again is a human child, how it learns to spek it's native language by mimicking it's parents and observing the environement. The best example in machines would be the robo dogs. Prior to the AI based algorithm in robo dogs they used ta pre defined algorithm where it teaches the dog how to walk but it was not that effective, after using the machine learning techniques where the dog was only taught basic things which it can do and what is a good sign or progress or a reward that is taking a step further and what is the opposite, i.e. falling down it tried to took more of former steps than the later ones and that's how it stores what it learned and that way it was able to mimic the real dogs more aptly. This is called Reinforment learning and it consists of following things:
1. Environment
1. Agent
1. Action

### Environment:
The Environment is the outer world from which the agent senses, i.e. takes input 

### Agent:
Agent is our robot which takes an input and do some process on it and takes a decision.

### Action:
The process done to take the decision by the agent is called Action. After performing an action the agent's state is changed and based on it's actions it gets a reward or a punishment.

#### _Image to be added_
