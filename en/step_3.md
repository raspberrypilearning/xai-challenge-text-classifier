
## Train the model

Imagine having a treasure chest full of fun quotes from your favourite movie characters, both the good guys (heroes) and the not-so-good guys (villains), with the quotes in two big piles — one for the heroes and one for the villains. In the world of machine learning, these piles are called "classes". The `hero` class is filled with all the cool things the heroes say, and the `villain` class has all the catchy phrases from the villains. On the back of each quote is a `label` that says whether the quote is a `hero` or a `villain` quote. 

Now let's say we find a **new** quote; one we've never seen before, which has no label. A machine learning model analyses this new quote and checks if it matches the pattern detected for the hero pile or the pattern for the villain pile. The model does not guess or understand, it just detects patterns. The model then predicts whether the new quote is from a hero or a villain, together with a measure of certainty.

--- task ---

Select **Add new label**. 
![Image showing the button which reads Add new label.](images/add_new_label.png)
--- /task ---

--- task ---

In the window that pops up, create a label for the `hero` class.
![](images/add_hero.png)

**Repeat** this step to create a second label for the `villain` class.

--- /task ---

You should now see two empty boxes, one titled 'hero' and one titled 'villain':
![](images/text_model.png)

--- task ---

Look in your favourite books, or search online for quotes from famous heroes. In your `hero` class, click **Add example** and paste or type in the quotes one at a time. 
![Button that reads '+ add example'](images/add_example.png)

To make it a bit easier, we have also provided a [spreadsheet](https://docs.google.com/spreadsheets/d/1Ge1xmn6gPoQhs78Rh5CQKVKYwNRW_9yOdhehtsKEFwo/edit?usp=sharing){:target="_blank"} with loads of quotes for you to use: there's a tab for `hero` quotes, a tab for `villain` quotes, and another tab for `TESTING DATA`. **Do not use the TESTING DATA in this step — you will need it later!**

--- /task ---

--- task ---

Continue to add quotes until you have input a selection of quotes you are happy with. The more quotes you have for each class, the more accurate your model will be.

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

You will have to wait a few moments for the model to train.

--- /task ---

### Test your model

Now that you have trained your model, it is time to test it to see how successful it is.  

--- collapse ---
---
title: Training data vs. testing data
---

To train a machine learning model to classify a specific item, we provide it with a particular set of data called **training data**. This data set is similar to the exercises in a textbook that have answers; they help in understanding and practising the topic.

After the model has processed the training data, it's essential to check its performance. For this, we introduce the model to a new set of data known as **testing data**. Think of this as taking a quiz or test at school: the questions aren't identical to what you practised, but they cover the same topic.

**Why keep them separate?**
If we use the same data for both training and testing, it's like giving you a maths test with the exact same questions you practised with. You might get all the answers right, but it doesn't show if you understand the topic broadly. It only shows that you know those specific questions.

Similarly, if we test the model with the same data it was trained on, we can't be sure if it has analysed enough data to make accurate predictions or if it has already classified that specific data during training. By using different data for testing, we can get a better idea of how well the model can classify **new** items of data.

So, it's essential to keep the training and testing data separate to make sure you get a realistic assessment of how the model performs. 

--- /collapse ---


--- task ---

To see how successful your model is at classifying heroes and villains, test your model by pasting or typing a quote into the field that appears.

**IMPORTANT:** Make sure you don't use a quote that already exists in your training data! If you are using the quotes from the [spreadsheet](https://docs.google.com/spreadsheets/d/1Ge1xmn6gPoQhs78Rh5CQKVKYwNRW_9yOdhehtsKEFwo/edit?usp=sharing){:target="_blank"}, make sure to use quotes from the TRAINING DATA tab! 

--- /task ---

--- task ---

Click the **Test** button to test your model. Your model will predict whether the text you entered is heroic or villainous and will tell you the level of confidence the model has in that prediction.

![](images/test_text.png)
In this example, the model is only 19% certain the quote from the Wizard of Oz is spoken by a hero (it is — Dorothy says it!). 19% is not a very good confidence score; most commercial classification applications need to operate at around 95–99% confidence!

--- /task ---

--- task ---

Once you have tested a few different quotes, think about these important things and add your answers to your Blueprint:

1. Describe the results of your testing. How accurate was the model? 
2. Why do you think the prediction is sometimes wrong?
3. How could you improve the accuracy of the model?

--- /task ---

--- collapse ---
---
title: Bias and data
---

When we train a model to classify different things, like dogs and cats, we need to give it lots of examples. These examples are called **training data**.

If we use a training data set that contains mostly small dogs and large cats, this does not accurately represent the real world as there are also large dogs and small cats. If the training data is not representative of what you want to model, the model is more likely to output an incorrect prediction.

This is called **bias**, which means the model favours one thing over another. We can fix this by using a more diverse training data set that includes different sizes, colours, and breeds of dogs and cats. By doing this, we can help the model identify the features that distinguish each type of animal, rather than just relying on the animal's size.

--- /collapse ---

<p style='border-left: solid; border-width:10px; border-color: #0faeb0; background-color: aliceblue; padding: 10px;'>
Imagine you were making an app that classified the tone of written messages.
<br><br>
Now think of ten books or articles you could use to gather text samples for your training data. What bias might you introduce? Have you picked texts from a variety of genres? Would your app work with messages written by people from all over the world with different cultural backgrounds and languages? Have you got quotes from characters of all genders?
<br><br>
By using more diverse and representative training data to avoid <strong>bias</strong>, we can help ensure that the app classifies text accurately and fairly when it encounters new examples. This can make the app more useful and reliable for different applications, from filtering comments online to helping editors understand the tone of articles.
</p>
Let's start making your machine learning application and think about what it will do!
