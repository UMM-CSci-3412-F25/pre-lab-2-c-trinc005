# Leak report

_Use this document to describe whatever memory leaks
you find in `clean_whitespace.c` and how you might fix
them. You should also probably remove this explanatory
text._

The leak I found in 'clean_whitespace.c' was found on lines 
36 and then 56. The leak in line 36 could not be handled under
the same function because it was directly attached to the returned result.
What I had to do to fix the memory leak was to free up the memory leak 
on line 56. I used an if statement to check if the string was empty or not
and if it was not empty then it freed the allocated memory.

Like wise the memory leaks in the test were fixed by assigning each strip
function to a single variable and then clearing that variable at the end of each 
test that had a memory leak.