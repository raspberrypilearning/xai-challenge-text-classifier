
## Train the model

Imagine having a treasure chest full of fun quotes from your favorite movie characters, both the good guys (heroes) and the not-so-good guys (villains), with the quotes in two big piles - one for the heroes and one for the villains. In the world of machine learning, these piles are called "classes". The `hero` class is filled with all the cool things the heroes say, and the `villain` class has all the catchy phrases from the villains. On the back of each quote is a `label` that says whether the quote is a `hero` or a `villain` quote. 

So let's say we find a *new* quote; one we've never seen before, which has no label. A machine learning model takes a peek at this new quote and checks if it matches the patterns it learned from either the hero pile or the villain pile. It's not guessing or understanding, it's just spotting patterns. The model then predicts whether the new quote is from a `hero` or a `villain`, with an amount of certainty.

--- task ---

Select **Add new label**. 
![an image showing the button which reads Add new label](images/add_new_label.png)
--- /task ---

--- task ---

In the window which pops up, create a label for the `hero` class.
![](images/add_hero.png)

**Repeat** this step to create a second label for the `villain` class.

--- /task ---

You shouls now be looking at an two empty boxes, one title 'hero' and one titled 'villain:
![](images/text_model.png)

--- task ---

Look in your favourite books, or search online for quotes from famous heroes. In your `hero` class, click `Add Example` and paste or type in the quotes one at a time. 
![Button which reads '+ add example'](images/add_example.png) 

--- /task ---

--- task ---

Repeat this process a number of times until you have collected a bank of quotes you are happy with. The more quotes you have for each class, the more accurate your model will be.

![](images/villain_class.png)

--- /task ---

--- task ---

Select **Back to project**.
![](images/back_to_project.png)

--- /task ---

--- task ---

Next, select **Learn & Test**.

![](images/learn_test.png)


Your model is now ready to be trained. 

--- /task ---

--- task ---

Select **Train new machine learning model**.

![](images/train_new.png)

You will have to wait a moment for the model to train.

--- /task ---

### Testing your model

Now that you have trained your model, it is time to test it to see how successful it is.  

--- task ---

To see how successful your model is at classifying heroes and villains, test your model by typing in a quote.
![](images/test_text.png)

--- /task ---

--- task ---

Click the **Test** button to test your model.

--- /task ---

--- task ---

Once you have tested a few of the images, answer the following questions in your **blueprint**:

1. Describe the results of your testing. How accurate was the model? 
2. Why do you think the prediction is sometimes  wrong?
3. How could you improve the accuracy of the model?

--- /task ---

### Bias and data

When we teach a computer to recognize different things, like apples and tomatoes, we need to give it lots of examples to learn from. These examples are called **training data**.

If we use a training dataset that contains mostly red tomatoes and green apples, this does not accurately represent the real world as there are also red apples and even green tomatoes. If the data used to train the model is not representative of what you're trying to model, neither will the prediction be which your model makes.

This is called **bias**, which means the computer is favouring one thing over another. We can fix this by using a more diverse training dataset that includes different types and colours of apples and tomatoes. By doing this, we can help the computer learn to recognize the features that distinguish each type of fruit, rather than just relying on the colour of the training examples.

<p style='border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;'>
By using more diverse and representative training data, we can help ensure that the computer makes accurate and fair predictions when it encounters new examples. This can make the computer more useful and reliable for different applications, from identifying objects in photos to making decisions in healthcare or finance.
</p>

Let's start making your machine learning application and think about what it will do!
