dd: delete sentence

J: join 2 lines together

o:  creates a new, empty line BELOW the cursor and puts Vim in Insert mode.

O: open a line ABOVE the cursor

w: move cursor forward one word

e: move to the next end of the word

b: move to the beginning of the word

0: move to the first character of the line

$: move to the end of the line (3$: move to the end of 3rd line)

^: moves to the first non-blank character of the line.

f+letter: find word begining with that letter to the right

F+letter: find word beginning with that letter to the left

G: go to the end of the file == L (last)

gg: go to the start of the file == H(home)

ctr + G: where’s the file is at

ctrl + d # ctr + u

ctr + s : split horizontal # ctr+v: split vertical

v: highlight text

shift + v + j/k: highlight the whole line

ctr-e: scrollup an extra line # ctr-y scrolldown

ctr-f: scroll forward # ctr-b: scroll backwards

``: go back to the old position before the jump

ctr+ o: go to older position # ctr-i go to newer position

ma: create a mark, `a: go to that mark

dd: delete the whole line

cc: change the whole line

d$ or D: delete to the end of line

c$ or C: change to the end of line

r + letter: replace a letter under the cursor with a new letter

df> and then . to delete tag, i.e: '<b></b>'

ctr + r: redo # ctr + u: undo

==Change one word to another multiple time:==
i.e: change 4 "four"s to "five"

/four<enter>

cwfive<esc>

n

.

n

.

=end=

y: copy

p: paste a line after the current line cursor on

P: paste a line before the current line cursor on

:%s/pattern//gn :count number of matches of a pattern

:3s/pattern//gn: check to see if that pattern is on line 3

shift + i : open hidden files


NERDTREE - vim: 

u: move up a dir from the selected dir/file # C: move to the selected dir

U: move up a dir but leave the selected one open

m: open menu

For files:

o (go): open ## go

s (gs): open file vertically split # i (gi): open file horizontally split

t: open file in new tab (T open new tab silently)

For directories:

o: open & close ## O: recursively open

x: close parent ## X: close all children recursively

e: explore selected dir

p: go to parent

P: go to root

K: go to first child # J: go to last child

Ctrl-k: go to prev sibling # Ctrl-j: go to next sibling

I: hidden files

F: only list files


