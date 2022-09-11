---
title: "Word List Sorter"
excerpt: "Alphabetically sorts and filters a list of words to be used as input to a learn-to-type website"
collection: projects
---
This project was made to aid me in learning to type faster. And by that I don't mean learning to type faster, I mean learning to type ... faster. For too long, I had been guilty of all the big typing sins: looking between the keyboard and the monitor, hunting-and-pecking for keys, not using my right pinky, but no longer. I started my learning journey on <a href="https://www.keybr.com/" target="_blank">Keybr</a>, where I learned how to touch type. I then moved to other sites to improve my speed and accuracy. I soon noticed, however, that a lot of the words I knew well were being repeated, and the process felt inefficient. This is where my program came in. I used <a href="https://monkeytype.com/" target="_blank">Monkeytype</a> to discover which words took longer for me to type and compiled them into a list. On <a href="https://10fastfingers.com/" target="_blank">10fastfingers</a>, there is a form where you can enter a custom word list to practice specific words. Utilizing both websites with my program, I practiced the words that I was least familiar with, and I learned to type faster.

Design process
-----
The main goal for this project was to assist me in entering practice typing words into a list. Over my practice sessions, I compiled quite a long list of words, many of which were duplicates. The program was made to sort the list and filter out any repeats. This way, when needed, I can add more words to the list worry free.

The program is a .NET Framework console application written in C#. This means the program can run on Windows machines from the command-line. I created two objects: a file gateway and a word list each with their own methods. The file gateway is used to retrieve and save files, and the word list is used to sort and filter the list of words.

This project's GitHub repository can be seen <a href="https://github.com/noahcoleman42/WordListSorter" target="_blank">here</a>.

Try it out
-----
If you would like to use this (and are using a Windows machine), follow these steps:

1. Clone my repository and change the file path on lines 20 and 32 of Program.cs to a location on your machine. They should look like this:
    ```
    aListOfWords = aFileGateway.GetWordList(@"C:\Users\<your_username>\Desktop\WordsForTypingPractice.txt");
    ```
    ```
    aFileGateway.SaveWordList(@"C:\Users\<your_username>\Desktop\WordsForTypingPractice.txt", aListOfWords);
    ```
2. Make a new file on your Desktop named WordsForTypingPractice.txt and add the words you wish to practice separated by a '\|' character.
3. Run WordListSorter.exe from \\bin\\Debug\\.

That's it! After copying the text and pasting it into the <a href="https://10fastfingers.com/" target="_blank">10fastfingers</a> custom typing test form, you are ready to learn to type faster!
