permalink: /404.html
# Week 5 Lab Report
## `grep` ##

This lab works to provide information on the `grep` command and offer alternate command-line options. This command will execute itself by searching a file for the given string.

For each alternate command-line option, there will be 3 examples provided in the `./technical` directory which follow:
```
technical/
    911 report/
    biomed/
    government/
        About_LSC/
        ALcohol_Problems/
        Env_Prot_Agen/
        Gen_Account_Office/
        Media/
        Post_Rate_Comm/
    plos/
```

To find information about each command, I used the `man <command>` in the terminal and recieved an output that looked like this:

 ![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-10-31%20at%203.26.58%20AM.png?raw=true)

## **COMMANDS**
## `grep -e`    gives the patern of the String you input.
## `grep -i`    will ignore the uppercase vs lowercase Strings.
## `grep -c`    counts the amount of times your inputted String appears in a text.

## Example #1- 
In this example, we will be using the path:
```
technical/
    911report/
        chapter1.txt
```
to find where the String "Tuesday" appears: 

```dotnetcli
grep -e "Tuesday" ./technical/911report/chapter-1.txt
```

![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%2010.05.05%20PM.png?raw=true)

As you are able to see, it allows us to have enough context as to where the String is coming from.

Since Tuesday is always spelled with an uppercase 'T', what would happen if we wanted to search "tuesday"? The command would not find anything, which is where `grep -i` becomes important.
```dotnetcli
grep -i "tuesday" ./technical/911report/chapter-1.txt
```
This will find the String no matter if it is typed with an uppercase or lowercase 'T' in the file. Thus, we get the same output as we did with `grep -e`:

### ![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%2012.43.57%20PM.png?raw=true)

To see how often this word appears, we could not use the same command and will therefore use `grep -c`

```dotnetcli
grep -c "Tuesday" ./technical/911report/chapter-1.txt
```
This is going to count how many times ***Tuesday*** is written and we get this output:

### ![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%2012.51.26%20PM.png?raw=true)

Meaning ***Tuesday*** appeared 3 times total.

## Example #2-
The path for the second example of the alternate commands will be:
```
technical/
    plos/
        journal.pbio.0020042.txt
```
To use this file and search the contents, we need the path. In this instance, **plos** contains a lot of files and it can be difficult to search for a particular one. In order to narrow down the **.txt** files, we must use the **find** command. In this case, we start from the **./technical** directory and find the **plos** path.
```dotnetcli
find ./technical > plos
```
From here, the **grep** command is simple and we want to use the last few digits of the specific .txt file we are looking for
```dotnetcli
grep "42.txt" plos
```
These two commands will easily locate the path of the file:

![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%2010.55.49%20PM.png?raw=true)

In this file, I want to search for the term "coli". I will do so by using our command
```dotnetcli
grep -e "coli" ./technical/plos/journal.pbio.0020042.txt
```
By doing this, we easily find the pattern of our String:

![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%203.30.46%20PM.png?raw=true)

Since the string 'coli' is typically not a term on its own, there will not be any uppercase versions of it in this file. Thus using the command-line option 
```dotnetcli
grep -i "coli" ./technical/plos/journal.pbio.0020042.txt
```
we will get the same output again:

![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%203.39.53%20PM.png?raw=true)

Counting the amount of times will be the same as in Example #1 using a different path
```dotnetcli
grep -c "coli" ./technical/plos/journal.pbio.0020042.txt
```

### ![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%203.43.07%20PM.png?raw=true)
As we can see, it happens to appear the same amount of times as ***Tuesday*** did in the previous example.

## Example #3-
Our last path we will be using is:
```dotnetcli
technical/
    government/
        Media/
            water_fees.txt
```
If we go into a more embedded file, the grep command will be extremely helpful in locating the file's path. Once it is located it is easy to find a term such as "water" within the specific file

To **find** the pattern we use
```dotnetcli
find ./technical > Media
```
If we were to find every file, using
`ls` if would give you a lot to sort through

![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%2011.17.42%20PM.png?raw=true)

`grep` is a much more simple solution because I can narrow the path down to the exact file I am looking for

![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%2011.13.33%20PM.png?raw=true)

Say I am looking for the term ***water*** so I use 
```dotnetcli
grep -e "water" ./technical/government/Media/water_fees.txt
```
My output seems to be:

### ![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%2011.28.47%20PM.png?raw=true)

The only issue is; in this text, ***Water** with an uppercase 'W' appears and it isn't accounted for unless we use our alternate
```dotnetcli
grep -i "water" ./technical/government/Media/water_fees.txt
```
Now, instead the output looks like:

### ![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%2011.34.52%20PM.png?raw=true)

Which as we can see, is longer than the previous text.

Considering we don't want to go through each String and count this word we will once again use
```dotnetcli
grep -c "water" ./technical/government/Media/water_fees.txt
```
The issue is that this will only count the word water with a lowercase 'w'. If we want both uppercase and lowercase counted, they need to be added together. So will will preform two commands:
```dotnetcli
grep -c "water" ./technical/government/Media/water_fees.txt

grep -c "Water" ./technical/government/Media/water_fees.txt
```
Our two outputs are:

![](https://github.com/jraynovi/lab-week-5/blob/main/Screen%20Shot%202022-11-03%20at%2011.42.43%20PM.png?raw=true)

Meaning once we add them together, we get a total of the word ***water*** 19 times.
