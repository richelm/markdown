<link
	href="https://rawgit.com/richelm/markdown/master/markdown.css"
	type="text/css"
	rel="stylesheet"></link>


# Sample Markdown File

[MSUID]: https://www.msu.edu "MSU Main Web Site"

<a name="paragraphs" />

## Paragraphs of Text

### What is Lorem Ipsum?

**Lorem Ipsum** is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section 1.10.32.

## List

### Ordered List

1. This is an ordered list.
1. Second line of list.
1. Third list item.
1. A Forth item

### Un-ordered List

* This is an un-ordered list
* Second bullet item
* And the third bullet item

### More Complex List

1. Top level items are ordered
	* Second level items are un-ordered
1. Next top level
	* Do these things:
		1. Wash dishes.
		1. Vacuum carpets
		1. Do laundry
		1. Take dog for a walk
	* When TODOs are done:
		1. Take a nap.
		1. Watch movie.
1. One more top level
	* Is this complex list example good enough?

## Commands and Code Segments

Issue the following command to copy file1 to file2 `cp file1 file`

The following **SQL** will select the *last_name* column from the *name* table in alpha sort order:

		select last_name
		from name
		order by last_name

Some of you may write your SQL so that it is more readable:

		select
			n.last_name,
			n.first_name,
			a.email
		from
			name n
			inner join address a
			on n.emp_id = a.emp_id
		where
			n.emp_start_date > "7/1/2000"
		order
			by last_name

## Links

Goto the main [MSU Website][MSUID] for information about Michigan State University.

This first place to get an answer to your question is [Google](https://google.com/ "Click here to go to Google Search"). What happens when you hover over the *Google* link?

Where did we discuss [paragraphs](#paragraphs)?

You can read all about the Markdown syntax at [Daring Fireball](http://daringfireball.net/projects/markdown/syntax "Markdown Syntax Explained").

## How Do I Convert Markdown to HTML?

There is a perl script for that. Here are the basic steps:

1. Download the Markdown.pl script from [Daring Fireball](http://daringfireball.net/projects/markdown/)
1. Put it somewhere on your computer, say `/home/sparty/bin`
1. Make an alias

		alias md="perl /home/sparty/bin/Markdown.pl"

1. Convert the file

		md sample.md > sample.html

Of course you could setup a *makefile* or use *Apache ANT*, but the whole idea behind Markdown is to keep it simple.


## Where is the Source for This Document?

It is right [here](./sample.text).

-----
&copy; 2015 Michigan State University

</body>
</html>
