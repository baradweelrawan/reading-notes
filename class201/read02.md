# this is read02 from 201
# HTML :
![img](https://upload.wikimedia.org/wikipedia/commons/thumb/6/61/HTML5_logo_and_wordmark.svg/1200px-HTML5_logo_and_wordmark.svg.png)

# Text:
When creating a web page, you add tags known as markup to the ontents  of the page. These tags provide extra meaning and allow browsers to show users the appropriate structure for the page.

 1. Headings: HTML has six "levels" of headings:
    * <h1> : is used for main headings
    * <h2> is used for subheadings
    * <h3>
    * <h4>
    * <h5>
    * <h6>
2. Paragraphs <p>: To create a paragraph, surround the words that make up the paragraph with an opening <p> tag and closing </p> tag. 

3. Bold & Italic :
  * <b> represents a section of text that would be presented in a visually different way .
  * <i> represents a section of text that would be said in a different way from surrounding content.

# Line Breaks & Horizontal Rules :
  1. <br /> :the browser will automatically show each new paragraph or heading on a new line. But if you wanted to add a line break inside the middle of a paragraph  .
  2. <hr /> :To create a break between themes — such as a change of
topic in a book or a new scene in a play — you can add a horizontal rule between sections.

# Semantic Markup :
There are some text elements that are not intended to affect the
structure of your web pages, but they do add extra information to the
pages — they are known as semantic markup.

# Strong & Emphasis:
1. <strong> :indicates that its content has strong importance.For example, the words contained in this element might be said with strong emphasis.
2. <em> : indicates emphasis that subtly changes the meaning of a sentence.

# Quotations :
1. <blockquote> :used for longer quotes that take up an entire paragraph. Note how the <p> element is still used inside the <blockquote> element.
2. <q> :used for shorter quotes that sit within a paragraph. Browsers are supposed to put quotes around the <q> element.

# JAVA SCRIPT :

![img](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQwQoZYCmlCWPeqofw3GA4rP3ixT3X9_O7bI9dajwAGDXpaF1AWkpcMIjH96BOMFVkLRIA&usqp=CAU)

# Basic JavaScript Instructions :
1. STATEMENTS :A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a statement. Statements should end with a semicolon.JavaScript is case sensitive.statement is an individual instruction that the computer should follow. Each one should start on a new line and end with a semicolon. This makes your code easier to read and follow.The semicolon also tells the JavaScript interpreter when a step is over, indicating that it should move to the next step.
2. COMMENTS :You should write comments to explain what your code does.
They help make your code easier to read and understand.This can help you and others who read your code.
  * MULTI-LINE COMMENTS :To write a comment that stretches over more than one line, you use a multi-line comment, starting with the /* characters and ending with the * / characters.Anything between these characters is not processed·by the JavaScript interpreter.
  * SINGLE-LINE COMMENTS :In a single-line comment, anything that follows the two forward slash characters I/ on that line will not
be processed by the JavaScript interpreter. Singleline comments are often used for short descriptions of what the code is doing.

# WHAT IS A VARIABLE? :
 A script will have to temporarily store the bits of information it
needs to do its job. It can store this data in variables.When you write JavaScript, you have to tell the interpreter every individual step that you want it to perform. This sometimes involves more detail than you might expect.A variable is a good name for this concept because the data stored in a variable can change or vary each time a script runs.

# DATA TYPES :
JavaScript distinguishes between numbers,strings, and true or false values known as Booleans.
 1. NUMERIC DATA TYPE
 2. STRING DATA TYPE
 3. BOOLEAN DATA TYPE
 
# CHANGING THE VALUE OF A VARIABLE :
Once you have assigned a value to a variable, you can then change what is stored in the variable later in the same script.Once the variable has been created, you do not need to use the var keyword to assign
it a new value. You just use the variable name, the equals sign also known as the assignment operator, and the new va lue for that attribute.

# RULES FOR NAMING VARIABLES :
1. The name must begin with a letter, dollar sign ($),or an underscore (_). It must not start with a number.
2. The name can contain letters, numbers, dollar sign ($), or an underscore (_). Note that you must not use a dash(-) or a period (.) in a variable name.
3. You cannot use keywords or reserved words. Keywords are special words that tell the interpreter to do something. 
4. All variables are case sensitive, so score and Score would be different variable names, but it is bad practice to create two variables that have the same name using different cases.
5. Use a name that describes the kind of information that the variable stores.
6. If your variable name is made up of more than one word, use a capital letter for the first letter of every word after the first word.

# ARRAYS :
An array is a special type of variable. It doesn't just store one value; it stores a list of values.Arrays are especially helpful
when you do not know how many items a list will contain because, when you create the array, you do not need to specify how many values it will hold.If you don't know how many items a list will contain, rather
than creating enough variables for a long list when you might only use a small percentage of them, using an array is considered a better solution.
# CREATING AN ARRAY :
You create an array and give it a name just like you would any other variable using the var keyword followed by the name of the array.The values are assigned to the array inside a pair of square brackets, and each value is separated by a comma. The values in the array do not need
to be the same data type, so you can store a string, a number and a Boolean all in the same array.
# VALUES IN ARRAYS :
Values in an array are accessed as if they are in a numbered list. It is important to know that the numbering of this list starts at zero not one.
1. NUMBERING ITEMS IN AN ARRAY:Each item in an array is automatically given a number called an index. This can be used to access specific items in the array.
2. ACCESSING ITEMS IN AN ARRAY:To retrieve the third item on the
list, the array name is specified along with the index number in
square brackets.
3. NUMBER OF ITEMS IN AN ARRAY:Each array has a property called
length, which holds the number of items in the array.

# ACCESSING & CHANGING VALUES IN AN ARRAY:
To access a value from an array,after the array name you specify the index number for that value inside square brackets.You can change the value of an item an array by selecting it and assigning it a new value just as you would any other variable using the equals sign and the
new value for that item.

# EXPRESSIONS :
An expression evaluates into (results in) a single value. Broadly speaking there are two types of expressions.
1. EXPRESSIONS THAT JUST ASSIGN A VALUE TO A VARIABLE