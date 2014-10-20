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

There are 5 area of the main window:

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
3. Click "Choose" button to choose the target directory "bench" or you can type it by yourself.(complete path is needed)
4. Click "Preview" button to check the results, you should see the first 5 files' name in the previewer.
5. Click "Ok" button to create this new toekn.

You will see a new token in the token list of main window.

Now, let us write the script in script editor:

```
DOIT #
```

Then do `run` in the menu.

Greate! All commands are excuted!<br >
If you are familar with the process, it is really fast and simple(than any other script).

---

### Token

---

#### Create/Edit/Remove a token

#### Symbol

#### Type

#### Value

#### Preview

#### Filter

#### Decorater

---

### Run script as shell script

#### Just run it

#### Catch results

---

### Save and open sk files
