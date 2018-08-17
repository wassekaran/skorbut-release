![skorbut logo](https://i.imgur.com/J9j9MNs.png)

![first example](https://i.imgur.com/PlMxIbC.png)

## What is skorbut?

skorbut is a simple teaching environment for a subset of C with a memory visualizer.
If you ever had trouble visualizing arrays and pointers, you have come to the right place.

## Does the name mean anything?

*skorbut* is German for *scurvy*, an illness that is caused by a lack of Vitamin C.
skorbut also lacks C in the sense that it implements only a restricted subset of C.

## Where do I download skorbut?

Click [this download link](https://github.com/fredoverflow/skorbut-release/blob/master/skorbut.jar?raw=true).
If for some reason this doesn't work, click `skorbut.jar` in the list above, then `Raw` or `View Raw`.

## How do I start skorbut?

skorbut requires Java 8 or newer to run. Make sure you have Java installed!

On most operating systems, you can simply run a jar by double-clicking on it.

If double-clicking does not start the system, open a terminal inside the download folder and write:

    java -jar skorbut.jar

## How do I save my code?

The code is automatically saved to a new file each time you click the start button.
The save folder is named `skorbut`, and it is located in your home directory.
The full path is displayed in the title bar.

## Does skorbut support auto indentation?

Yes, just hit Enter or Tab.

## What about auto completion?

Not yet...

## What features of C are currently missing?

Non-exhaustive list off the top of my head:

| Feature             | Priority |
| ------------------- | -------- |
| preprocessor        | very low |
| variadic functions  | very low |
| compound assignment | low      |
| casts               | low      |
| null pointer        | medium   |
| union               | very low |
| pass struct         | low      |
| return struct       | low      |

## Wait, no preprocessor? How do I `#include <stdio.h>`?

You don't need to include anything, the following standard library functions are already available:

- printf
- scanf
- putchar
- getchar
- malloc
- free
- realloc
- qsort
- bsearch

## What about my own header files?

skorbut does not support multiple translation units, so there would be no point in supporting header files.

## How do I define constants without `#define`?

For integral constants, you can use anonymous enumerations like `enum { N = 10 };`

## Aren't casts kinda essential in C?

Not really. Most casts in C are either unnecessary (like `float` to `int`) or invoke undefined behavior (like `float*` to `int*`).

Note that C allows assignment between `void*` and any other pointer type, so you can simply write:

    int * p = malloc(10 * sizeof(int));

## Is skorbut open source?

Not yet, but I will probably open-source skorbut when I lose interest in further development. Don't hold your breath though ;)
