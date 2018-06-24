Organization
============

While storing code in Github is good, there is a minor flaw that results from storage of files in Github. The flaw has no effct on whether code compiles, but it does have a significant effect on whether the code is able to be readable or accessible from other sources. One significant problem we the programming team encountered in the writing of code is the issue of Version Control. When one is to make major changed to the code in Git and one makes another major change to the code in Git, there will often be conflicting changes in the code and usually this leads to some merging errors.

An example of such an error being caused by this kind of programming miscommunication would be this:

Say Person A were to write a line of code declaring wheels:

```java
public Wheel lefty, righty, backy, backy2;

```

Now say Person B deleted the Wheel object lefty, then if Person A were to access the lefty Wheel object, there would be a merging error where the Wheel is there on Person A's computer, but not on Person B's computer.
