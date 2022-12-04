# Lab Report Week 7
In this lab report we will be using ```vim``` to edit files in insert.

## Part 1: Change the name of the ```start``` parameter to ```base```

The sequence of keys to press using code formatting:

```
/start <enter> ce base <esc> n n n  :wq <enter>
```
We use ```/start <enter>```, to find the instances of where ```start``` appears, to quickly locate the word. When we hit the <enter> key, the cursor will find this word.
\
```ce base``` will allow us to replace the word with base. Using ```ce``` replcaes the word from the location of the cursor until the end of the word, since our cursor is at the front of the word, it will change entire word. We must go into insert mode and change the word to ```base```. 
 
We can ```n .``` until each instance of ```start``` has been changed. This command: ```n```, similar to (```/```) we made earlier, gets the cursor to each instances ```start```, and ```.``` will repeat the last command we did, which, in our case is ```ce base``` (change the word to base). 

\
We can then press ```:wq <enter>``` to save and quit.

## Part 2: Timing: ```vim``` vs ```scp```

Editing with vim: 0:38 \
Editing with scp: 1:49 \ 

\
I need a lot more practice with vim, but I can see how much time it would save in the future.
