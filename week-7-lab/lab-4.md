# Lab Report Week 7
In this lab report we will be using ```vim``` to edit files in insert.

## Part 1: Change the name of the ```start``` parameter to ```base```

The sequence of keys to press using code formatting:

```
/start <enter> ce base <esc> n n n  :wq <enter>
```
We use ```/start <enter>```, to find the instances of where ```start``` appears, to quickly locate the word. When we hit the <enter> key, the cursor will find this word.
![](https://github.com/jraynovi/cse15l-lab-reports/blob/main/week-7-lab/Screen%20Shot%202022-12-02%20at%2011.53.00%20PM.png?raw=true)
### *We have found the first instance of ```start```.*
\
```ce base``` will allow us to replace the word with base. Using ```ce``` replcaes the word from the location of the cursor until the end of the word, since our cursor is at the front of the word, it will change entire word. We must go into insert mode and change the word to ```base```. 
 
We can ```n .``` until each instance of ```start``` has been changed. This command: ```n```, similar to (```/```) we made earlier, gets the cursor to each instances ```start```, and ```.``` will repeat the last command we did, which, in our case is ```ce base``` (change the word to base). 
![](7-3A-n.png)
*Typing ```n``` has found the next instance of ```start```.*
![](7-3B-DOT.png) 
*Typing dot repeats the change command we did previously.*
![](7-3C1-changed.png)
*All instances of ```base``` have now been changed.*

\
We can then press ```:wq <enter>``` to save and quit.

## Part 2: Timing: ```vim``` vs ```scp```

Editing with vim: 0:41 \
Editing with scp: 1:16 \
(times are in minutes) 

\
It would take time to get used to all the commands ```vim``` has, but to run remotely it would be much easier to use ```vim``` rather than ```scp``` because it allows us to not worry about the directory the file has to go into when being copied. \
I think the reason above (running remotely) would make me lean towards using ```vim``` when having to run programs remotely. Since I have a windows computer, however, I would not use ```vim``` to edit local files, so if that was a necessary part of the task I would ```scp```.
