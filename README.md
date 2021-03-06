# Static Library Makefile 

This program creates a static library out of all files within the Utils directory and links it to the main program in main.cpp. Any files that are added to the Utils directory are automatically compiled and added to the static library without needing to update the Makefile. Makefiles utilize `realpath` directory variables to avoid issues with relative paths.

## Commands
* compile: `make` or `make build`
* run: `make run`
* clean: `make clean`

## Make Documentation and Useful Tutorials
* https://www.gnu.org/software/make/manual/make.html
* http://www.cs.colby.edu/maxwell/courses/tutorials/maketutor/
* https://www.geeksforgeeks.org/static-vs-dynamic-libraries/
* [YouTube: Introduction to Makefiles (Paul Programming)](https://www.youtube.com/watch?v=_r7i5X0rXJk)

## Automatic Variables
https://www.gnu.org/software/make/manual/html_node/Automatic-Variables.html#Automatic-Variables

$@
The file name of the target of the rule.

$%
The target member name, when the target is an archive member. See Archives. For example, if the target is foo.a(bar.o) then ‘$%’ is bar.o and ‘$@’ is foo.a. ‘$%’ is empty when the target is not an archive member.

$<
The name of the first prerequisite.

$?
The names of all the prerequisites that are newer than the target, with spaces between them. If the target does not exist, all prerequisites will be included.

$^
The names of all the prerequisites, with spaces between them. 

$+
This is like ‘$^’, but prerequisites listed more than once are duplicated in the order they were listed in the makefile. This is primarily useful for use in linking commands where it is meaningful to repeat library file names in a particular order.

$|
The names of all the order-only prerequisites, with spaces between them.

$*
The stem with which an implicit rule matches (see How Patterns Match). If the target is dir/a.foo.b and the target pattern is a.%.b then the stem is dir/foo. The stem is useful for constructing names of related files.

## Pattern Rule Examples
https://www.gnu.org/software/make/manual/html_node/Pattern-Examples.html#Pattern-Examples

## Basics of Variable References
https://www.gnu.org/software/make/manual/html_node/Reference.html#Reference
