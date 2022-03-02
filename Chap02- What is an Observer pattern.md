## What is an Observer pattern?

An object (a.k.a Subject) maintains a list of its dependents known as observers. Then if a state is changed, the subject notifies all of its observers of changes usually by calling their methods.

![](Images/1.png)

 
The Observer pattern can also be defined as the relationship where one subject can signal its many watchers (or observers). Unintuitively, it is the subject calls out to its observers that respond, rather than the observers acting independently on the subject.

For Example, **Player Died** → This is an event/subject and other classes are observers(enemies, UI, Sound effects, etc) are observing this event. So the Observer pattern helps us to send signals to all these observers and each one of them can run their own executions after receiving the signal. 

When the player dies, the enemy will have a different logic, UI service will be doing showing some “Player Died” UI,  sound effects will also get triggered, etc. So to execute all these things when a particular event triggers, the observer pattern helps us to send the signal to all the observers in one go.

Now let's see how we can use the Observer pattern to implement an achievement system. To make an achievement system first of all we need to store the achievement data in some container. right? In order to do that you will need a scriptable object.
