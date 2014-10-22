script-king
===========

A Lightweight tool for writing and running scripts(Version-1.0)

===

### Environments

You have to install `Python3`:

* [Python](https://www.python.org/)

You should check the package `tkinter` is already installed.(Do not worry! `tkinter` is a default package of Python)

---

### How to get script-king

Just download from github tarball:

* [download script-king](https://github.com/dokelung/script-king/tarball/v1.0)

---

### Run script-king

It's easy, just type:

```sh
$ ./sk
```

and you will see the friendly interface of script-king.

---

### Introduction

#### Why script-king?

#### Introduction of main window

Following is the graph of script-king main window():

![script-king main window](https://github.com/dokelung/script-king/blob/master/img/sk-main_win.png)

There are 5 area in the main window:

1. Window title: list tool's name, version and the current file name.
2. Menu bar: including all functions.
3. Token area: list the existing tokens and you can also create/delete/edit/move a token by the buttons aside.
4. Script editor: write the main script here with normal text and the token set already.
5. status bar: show the status of each actions.

---

### A quick example

Let me show you how to use and when to use script-king by a simple example.

First, assume you have a exutable file(command) named "DOIT".<br >
This command takes a file name as its parameter.<br >
Like that:<br >

```sh
$ DOIT FILE_NAME
```

Now, you have to run it with 100 files in directory "bench":

```
bench
  |--f1
  |--f2
  |--f3
  |...
  |--f100
```

I think you do not want to type the command 100 times.<br >
What can you do?<br >
Maybe a script: bash script, python script, ...<br >
Oh, but you are not familiar with any kind of script.(Yes, you are the expected user of script-king.)<br >
Or you think write the normal script is a trouble.<br >

The answer is ... using script-king!<br >

First, we have to set a token to reprents these 100 files.<br>
Click "create" button and you will see a token window:<br>

![script-king token window](https://github.com/dokelung/script-king/blob/master/img/sk-token_win.png)

Let's fill in some input fields to create a token:

1. Symbol: eacn token needs a symbol, now we choose `#` as `Symbol`.
2. Type: we want to iterate all file names of the directory "bench", so we type "iter" as `Type`.
3. Click `Choose` button to choose the target directory "bench" or you can type it by yourself.(complete path is needed)
4. Click `Preview` button to check the results, you should see the first 5 files' name in the previewer.
5. Click `Ok` button to create this new token.

You will see a new token in the token list of main window.

Now, let us write the script in script editor:

```
DOIT #
```

Then do `run` in the menu.

Greate! All commands are excuted!<br >
If you are familar with the process, it is really fast and simple(than any other scripts).

---

### Token

Token is a main object of script-king.<br >
We use token's symbol to represent some values.
You can simply think tokens are like variables. 

---

#### Create/Edit/Remove a token

You can use button `Create` or `Create` option in menu to create a new token.<br >
Choose an existing token then it can be edited by the `Edit` button or `Edit` option in menu.<br >
Choose an existing token then use `Delete` or `Delete` option in menu to remove it.

#### Symbol

A symbol is like a literal.<br >
We would use symbols to represent something in our scripts.

A letter, a word, or any syntax is avalible.<br >
But the blanks are not allowed for symbol.

#### Type

There are 3 types of token.

`fix`:  this token just represents a constant string, it is usually used to represent a directory name.<br >
`iter`: this token represents the files names in a specified directory.<br >
`num`:  this token represents numbers from the specifed range.

#### Value

#### Preview

After setting symbol, its type and its value, you can click `Preview` to check the first 5 items of this token.

#### Filter

Filter allows user to reserve some items and remove the others from a token.
It uses the if statement of python.

For example, if we want to resere the file names which contain string '.f' from a token whose symbol is #.<br >
We can write following sentence in filter:

```python
if '.f' in '#'
```

note that the symbol should be in the single quotation marks ''.

#### Decorator

script-king also supports other python statements.<br >


---

### Script convertion

---

### Run script as shell script

#### Just run it

#### Catch results

Choose the `Run and catch` option in menus to run the script and save the results to a specified file.

---

### Save and open sk files

You can save the current project to a sk file and reload it after.

Choosethe 
