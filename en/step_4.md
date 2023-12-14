
## Make a Scratch application to classify quotes

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
Your model is trained, tested, and ready to use, but to do that you need to create a Scratch project that allows your user to input text and classify the input as heroic or villainous.
</div>
<div>
![Image showing four screenshots of different Scratch classification applications.](images/demo_shot.png){:width="300px"}
</div>
</div>


### **Your project will:**
+ Take text input from the user
+ Use your trained ML model to classify text
+ Tell the user whether the input is from a 'hero' or 'villain'

--- task ---

On your [**project page**](https://machinelearningforkids.co.uk/#!/projects){:target="_blank"}, select **Make**:
![Image showing a button reading Make and the explanation 'Use the machine learning model you've trained to make a game or app, in Scratch, Python, or App Inventor'.](images/make_button.png)

--- /task ---

--- task ---

On the next page, select **Scratch 3**.
![](images/scratch3_button.png)

--- /task ---

<div style="display: flex; flex-wrap: wrap">
<div style="flex-basis: 200px; flex-grow: 1; margin-right: 15px;">
A special fork of Scratch will open in a new tab. When it does, you will see an item in the left-hand menu with the same name as your machine learning project.

The new grey blocks you can see in that menu allow you to access your machine learning model from within your project:
</div>
<div>
![Image showing several Scratch block menus, with the final one being titled MusicWellness with the Machine Learning for Kids logo.](images/model_blocks_menu.png){:width="100px"}
</div>
</div>

--- collapse ---
---
title: Pro tip: Save your work!
---

This special version of Scratch allows you to access your machine learning model, **but** if you try to open your project in another version of Scratch online **it won’t work**.

A solution to this is to save your work to your computer. Once you have the .sb3 file for your project saved, you can open it again later, or on another computer:
+ Go to [rpf.io/mlscratch](rpf.io/mlscratch){:target="_blank"} to get to this special fork of Scratch 
+ Once Scratch opens choose **File** > **Load from your computer**
+ Select your file in the window that appears to return to where you left off

![Image showing the Scratch file menu with the Load from your computer option highlighted.](images/load_menu.png)


Save your work as often as you can to make sure you don’t lose any progress!

--- /collapse ---

--- task ---

Add a `when green flag clicked`{:class="block3events"} block to your workspace. This is the script that will run the first time you start the project. 

```blocks3
when green flag clicked
```

--- /task ---

The next thing you want your application to do is ask the user to input some text — this is the text that will be compared by the model and classified as `hero` or `villain`.

--- task ---

In the blue `Sensing`{:class="block3sensing"} menu, add an `ask (What's your name?) and wait`{:class="block3sensing"} block:

```blocks3
when green flag clicked
ask [What's your name?] and wait
```

--- /task ---

--- task ---

Change the question text to ask your user to enter a quote. You could say something like:
+ What is your quote?
+ Halt! Who goes there?
+ Enter your favourite quote to start!
+ Type something to see if you are a hero or a villain!

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
```

--- /task ---

--- task ---

From the purple `Looks`{:class="block3looks"} menu, add a `say (Hello!)`{:class="block3looks"} block to your script.

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say [Hello!]
```

--- /task ---

Now, you're going to create the message your application will show the user when it has classified the text they entered. To do that, you're going to `join`{:class="block3operators"} some bits of text (called strings) with data from your machine learning model using specific blocks. 

The example message will say: "I am `(model confidence: number)`% certain you are a `(model label: hero/villain)`!

--- task ---

From the green `Operators`{:class="block3operators"} menu, place a round `join (apple) (banana)`{:class="block3operators"} block into the space in the purple `say`{:class="block3looks"} block:

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say ((join [apple] [banana]))
```

--- /task ---

--- task ---

Add another round `join (apple) (banana)`{:class="block3operators"} block into the gap in the block you just added (it doesn't matter which gap):

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join ((join [apple] [banana])) [banana])
```

--- /task ---

--- task ---

Add another round `join (apple) (banana)`{:class="block3operators"} block into the other gap in the `say`{:class="block3looks"} block:

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [apple] [banana]) ((join [apple] [banana])))
```
--- /task ---

--- task ---

Into the first space that says `apple`, type `I am `. 
Make sure you include a space at the end!

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [I am ] [banana]) (join [apple] [banana]))
```
--- /task ---

--- task ---

Into the second space, which says `banana`, drag a black `recognise text [text] (confidence)` block from the Machine Learning for Kids menu at the very bottom:

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [I am ] (recognise text [text] confidence :: #4b4c60)) (join [apple] [banana]))
```
--- /task ---

--- task ---

Into the next (third) space, which still says `apple`, type `% sure you are a `. 
Make sure you include a space at the end!

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [I am ] (recognise text [text] confidence :: #4b4c60)) (join [% sure you are a ] [banana]))
```
--- /task ---

--- task ---

Into the last (fourth) space, which still says `banana`, drag a black `recognise text [text] (label)` block from the Machine Learning for Kids menu at the very bottom:

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [I am ] (recognise text [text] confidence :: #4b4c60)) (join [% sure you are a ] (recognise text [text] label :: #4b4c60)))
```

--- /task ---

The final piece of the puzzle is to use the text your user entered as the information sent back to the model for classification!

--- task ---

From the light blue `Sensing`{:class="block3sensing"} menu, drop a round `answer`{:class="block3sensing"} bubble into the two white slots that say `text`:

```blocks3
when green flag clicked
ask [You there! What say you?] and wait
say (join (join [I am ] (recognise text (answer) confidence :: #4b4c60)) (join [% sure you are a ] (recognise text (answer) label :: #4b4c60)))
```

--- /task ---

--- task ---

**Click the green flag**, then type or paste some text into the prompt that appears and press **Enter**.

Your character will say whether the speaker of those words is a hero or a villain and to what certainty!

--- /task ---

In the next step, you can customise the way your application looks by adding costumes and some new features that activate depending on the classification of your input.

<p style='border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;'>
<strong>Text projects need to be retrained after 24 hours:</strong> If you are working on a text-based model, you will need to click the button to train your model if you have left it overnight or for more than 24 hours. Your training data will be stored online, but the model will time out after 24 hours. The model will need to be retrained at the start of each session; this should take only a couple of minutes.  
</p>


