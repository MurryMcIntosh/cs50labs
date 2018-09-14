# Hello

Hello, indeed! At right, in the *text editor*, is the very first program we wrote in C, in a file called `hello.c`. 

Click the folder icon, and you'll see that `hello.c` is the only file that's present at the moment. Per the mention of `/root/sandbox` below that icon, `hello.c` happens to be in a folder (otherwise known as a *directory*) called `sandbox`, which itself is in another folder called `root`. Click the folder icon again to hide all those details.

Next, in the *terminal window* at right, immediately to the right of the dollar sign (`$`), otherwise known as a *prompt*, type precisely the below (in lowercase), then hit Enter:

```
ls
```

You should see just `hello.c`? That's because you've just listed the files in that same folder, this time using a command-line interface (CLI), using just your keyboard, rather than the graphical user interface (GUI) represented by that folder icon. In particular, you executed (i.e., ran) a command called `ls`, which is shorthand for "list." (It's such a frequently used command that its authors called it just `ls` to save keystrokes.) Make sense?

Here on out, to *execute* (i.e., run) a command means to type it into a terminal window and then hit Enter. Commands are "case-sensitive," so be sure not to type in uppercase when you mean lowercase or vice versa.

{% next %}

Now, before we can execute the program at right, recall that we must *compile* it with a *compiler* (e.g., `clang`), translating it from *source code* into *machine code* (i.e., zeroes and ones). Execute the command below to do just that:

```
clang hello.c
```

And then execute this one again:

```
ls
```

This time, you should see not only `hello.c` but `a.out` listed as well? (You can see the same graphically if you click that folder icon again.) That's because `clang` has translated the source code in `hello.c` into machine code in `a.out` (which happens to stand for "assembler output," but more on that another time).

Now run the program by executing the below.

```
./a.out
```

Hello, world, indeed!

{% next %}

Now, `a.out` isn't the most user-friendly name for a program. Let's compile `hello.c` again, this time saving the machine code in a file called, more aptly, `hello`. Execute the below.

```
clang -o hello hello.c
```

Take care not to overlook any of those spaces! Then execute this one again:

```
ls
```

You should now see not only `hello.c` (and `a.out` from before) but also `hello` listed as well? That's because `-o` is a *command-line argument*, sometimes known as a *flag* or a *switch*, that tells `clang` to output (hence the `o`) a file called `hello`! Execute the below to try out that new and improved program.

```
./hello
```

Hello there again!

{% next %}

Recall that we can automate the process of executing `clang`, letting `make` figure out how to do so for us, thereby saving us some keystrokes. Execute the below to compile this program one last time.

```
make hello
```

And then execute the program itself one last time by executing the below.

```
./hello
```

Phew!