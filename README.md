-rolog Programming-
*A good website to practice Prolog is Swish*

*What is Prolog*
Prolog is a logic programming language. It takes a user to declare specific facts and rules for 
different senarios. Then the user will have to present an end goal, known as a query. An exmaple
of how this could be used it in finding terroist activies. It could also be used to help organizations
in decision-making. 


*How Prolog works*
In order to decribe relations in prolog you use clauses. Clauses are either facts or rules. A rule
is basically "this is true, if this is true". For example, this could be written in prolog as
"Head :- Body.". This statement would read as "Head is true, if Body is true". A fact is anything
that can be declared true. So if you wanted to say, "the sky is blue", you would write it in 
prolog as, "sky(blue).". Next you have a query which is where the user would ask a question. For
example, if you wanted to know if the sky was blue, you would write, "?- sky(blue).". In prolog,
all querries start with "?-". It's important to know that every line you enter has to be followed
by a period. Its like using a semicolon at the end of a line in C++. Also, anything that is in 
parentheses has to be lowercase. 

*Example of Prolog*
For this example, if you were given a family tree and wanted to see how people were related, this is how you would
do it. You will have to use what's called a compound term, which means that something
falls under the class of something else. It would be written as "father(jason, bradley).". This 
statement says that Jason is a father to Bradley. 

Jimmy and Stacy have a son James. James is married to Emily and they have a daughter named, Lindsey.

Jimmy			Stacy
	\			/
	 \		   /
	  \		  /
	   \	 /
		\   /
		James		Emily		
		   \		  /
		    \        /
			 \      /
			  \    /
			   \  /
			  Lindsey
			  
Prolog Code:

male(jimmy).
male(james).
female(stacy).
female(emily).
female(lindsey).
parent(jimmy, james).
parent(stacy, james).
parent(james, lindsey).
parent(emily, lindsey).
grandparent(X, Y) :- parent(X, Z), parent(Z, Y).

Now that we have some sample code, we can use the query to ask it questions.
This is how you would write the query:

?- parent(X, james).

The output is:

X = jimmy
X = stacy

If you said:

?- grandparent(X, lindsey).

The output is:

X = jimmy
X = stacy


**If you use the swish website to practice prolog, you dont put the "?-" when you type your query.
