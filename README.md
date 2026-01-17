### 0.5.0
version: YR #5
> Fixed:
-> Error YRPP0012: Invalid list element 'value', when you're trying to use a float/double as a list value.

!>> Out of support

Soon will new language arrive YR++ #1

>> Extended:
--> Library sys.io where extended from only one function os_() into 2 extra functions: 
- memory[b/kb/mb/gb]; shows amount of installed RAM on your PC
- battery(); current battery charge for laptops 

--> Library lists was also extended with new functions:
- pushlist(list, |list2|, >>/<<, index/end/begin); --> allows you to put a list2 into the list. Where >> means after index/begin/end and << means before index/begin/end of a list
- merge(list, index, index2); --> this function merges index with index 2 in one single element
- get(list, index); --> a second variant of getting a list element by index
- getremovedel(list); --> if you've deleted elements from a list you can get them in a variable but only the last deleted. If you need all of them you should use the parameter []. Usage: getremovedel(list, []); and you'll get all removed elements from chosen list as a mini list
- filter(list); --> removes all duplicates from a list
- sort(list, </>); --> sorting list elements. Parameter < is ascending (increasing) and > descending (decreasing). Also works with string lists.
- maxil(list); --> gets the biggest element value in a numeric list
- minil(list); --> the opposite of maxil().

>> Changed:
---> Library lists has 2 functions that were changed:
- remove(list, index); -> was the only variant for deletion one element at time. But in YR #5 there is an option of multiple deletion: remove(list, [index, index1, ..., indexN]);
- push(list, value/variable); was thy only element which could be added only at the end of a list. It was just like add(). But from now this function changes: 
push(list, index, <</>>, value/variable); --> it allows you to add an element before or after the chosen index. Note: push() doesn't work with empty list, while add() is working well.

---> Syntax was also changed for these functions:
Before          |   After        |
---------------------------------|
include <lib>;  |   include <lib>|
exclude <lib>;  |   exclude <lib>|
---------------------------------|
these functions are allowed to be used without ';'

>> Added:
----> New file extension
.garb is a file extension but it is more like an archive or place where you can leave useless or incorrect code. It could be executed and interacted

-----> New library: time
Functions----
- startc(); --> starts timer
- endc(); --> ends timer

----> Partial function import
using lib.[f1, ..., fN];

----> Possibility of using your own scripts in others
interact <userfile.yrpp/.rpp/.garb>~ --> where .yrpp, .rpp, .garb are supported file extensions

----> Acces to userfiles
There is a different syntax which depends on what are you trying to access
-------------------------------------------------------|
Function                    |   Variable               |
-------------------------------------------------------|
userfile::functionName()    |   userfile:~variableName |
-------------------------------------------------------|

>> Extra:
New command --help:
usage: .\Yrpp.exe --help
and you'll get the list of existing commands

YR got its own way of creation Console Apps by using this command:
.\Yrpp.exe --compile "Path\to\yrpp\or\other\supported\extension\file.yrpp" "output.exe"

Launching:
.\Yrpp.exe output.exe

Basic documentation could be found in this repository as "YR Doc"
