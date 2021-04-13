# this is read03
# The Structure of HTML
HTML it's  stands for Hyper Text Markup Language. first we are looking at how HTML is used to create web pages. You will see that you start by writing downthe words you want to appear on your page. You then add tags or elements to the words so that the browser knows what is a heading, where a paragraph begins and ends, and so on.

![HTML](https://th.bing.com/th/id/Rfde2937d347beb6659a8249ffb4a9691?rik=5xflhx2xFbhrEg&riu=http%3a%2f%2fquestbusinesssystems.com%2f25%2fhtml-logo-217.png&ehk=eQKGQ7P23ng19ztjeZ3t6zOg1ua%2bbW0rLhaUdJM8Tko%3d&risl=&pid=ImgRaw)

# How Websites Are Created :
All websites use HTML and CSS, but content management systems, blogging software, and e-commerce platforms often add a few more
technologies into the mix. Small websites are often written
just using HTML and CSS. Larger websites — in particular those that are updated regularly and use a content management system (CMS), blogging tools, or e-commerce software — often make use of more complex technologies on the web server,but these technologies are
actually used to produce HTML and CSS that is then sent to the
browser.
# how the web server that hosts the website you are visiting can be anywhere in the world:
 by the DNS servers that tell your browser how to find the website.
 The DNS server then tells the browser the location of the web
server hosting the site in specific location.
1. When you connect to the web,you do so via an Internet Service
Provider (ISP). You type a domain name or web address into your browser to visit a site.
2. Your computer contacts a network of servers called Domain Name System (DNS) servers.
3. The unique number that the DNS server returns to your computer allows your browser to contact the web server that hosts the website you requested. 
4. The web server then sends the page you requested back to your
web browser.
# HTML Describes the Structure of Pages :
The HTML code (in blue) is made up of characters that live inside angled brackets — these are called HTML elements. Elements are usually
made up of two tags: an opening tag and a closing tag.
 * The closing tag has an extra forward slash in it.Each HTML element tells the browser something about the information that sits between its opening and closing tags.
 ![HTML Structure ](https://th.bing.com/th/id/Rf31855b8f08e7687350b9fc49a77d839?rik=fbXLaOgV8y2NQA&riu=http%3a%2f%2fwww.basewebmaster.com%2fhtml%2fimages%2fpage-structure.gif&ehk=UDn6hDyfTM8bmdufpVoRtSYHvMt21RKffe3qwHw9Oko%3d&risl=&pid=ImgRaw)
 Tags tell you something about the information that lies between their opening and closing tags.

 # Extra Markup:
 there have been several different versions of HTML.Each new version was designed to be an improvement on the last with new elements and
attributes added and older code removed. 
 * HTML 4
 * XHTML 1.0

 # DOCTYPEs:
 Because there have been several versions of HTML, each web page should begin with a DOCTYPE declaration to tell a browser which version of HTML the page is using.

 # Comments in HTML:
 If you want to add a comment to your code that will not be visible in the user's browser, you can add the text between these characters:
                <!-- comment goes here --> 
  On a long page you will often see comments used to indicate where sections of the page start or end, and to pass on notes to help anyone who is looking at the code understand it.Comments can also be used around blocks of code to stop that code from being displayed
in the browser. In the example on the left, the email link has been
commented out.

# ID Attribute:
Every HTML element can carry the id attribute. It is used to uniquely identify that element from other elements on the page.It is important that no two elements on the same page have the same value for their id
attributes.It should start with a letter or an underscore not a number or any other character.The id attribute is known as a global attribute because it can be used on any element.

# Class Attribute:
Every HTML element can also carry a class attribute.Sometimes, rather than uniquely identifying one element within a document, you will want a way to identify several elements as being different from the other elements on the page.Its value should describe the class it
belongs to and on any element can share the same value. 
for example:  
         <p class="important">For a one-year period from
         November 2010, the Marugame Genichiro-Inokuma
         Museum of Contemporary Art (MIMOCA) will host a
         cycle of four Hiroshi Sugimoto exhibitions.</p>

# Block Elements:
It will always appear to start on a new line in the browser window.
Examples of block elements are: <h1>, <p>, <ul>, and <li>.

# Inline Elements:
It will always appear to continue on the same line as their neighbouring elements,and Examples of this are:<a>, <b>, <em>,<img>.

# Grouping Text &Elements In a Block:
* <div>:
allows you to group a set of elements together in one block-level box.
the contents of the <div> element will start on a new line, but other than this it will make no difference to the presentation of the page.

 # Grouping Text & Eleme nts Inline :
 * <span> :
 It acts like an inline equivalent of the <div>element. It is used to either:
   1. Contain a section of text where there is no other suitable
element to differentiate it from its surrounding text.
   2. Contain a number of inline elements .
 It used to control the appearance of the content of these elements using CSS, such that:a class or id attribute is used with <span> elements;To explain the purpose of this <span> element,So that CSS styles can be applied to elements that have specific values for these
attributes.

* IFrames:
An iframe is like a little window that has been cut into your page — and in that window you can see another page.One common use of iframes is to embed a Google Map into a page.
There are a few attributes that you will need to know to use it:
       1. src: specifies the URL of the page to show in the frame.
       2. height:specifies the height of the iframe in pixels.
       3. width:specifies the width of the iframe in pixels.
       4. scrolling:This is important if the page inside the 
          iframe is larger than the space you have allowed for it.
       5. frameborder:it indicates whether the frame should have
          a border or not. A value of 0 indicates that no border shouldbe shown. 
       6. seamless:it can be applied to an iframe where scrollbars
          are not desired.does not need a value, but you will often
          see authors give it a value of seamless.
# HTML5 Layout:  
is introducing a new set of elements that help define the structure of
a page.
* Traditional HTML Layouts:web page authors used <div> elements to group together related elements on the page (such as the elements that form a header, an article, footer or sidebar). Authors used class or id attributes to indicate the role of the <div> element in the structure of the page,and developers would usually put these main sections of the page inside <div> elements and use the class or id attributes to indicate the purpose of that part of the page. 
* New Html 5 Layout Elements:HTML5 introduces a new set of elements that allow you to divide up the parts of a page. The names of these elements indicate the kind of content you will find in them.The point of creating these new elements is so that web page authors can use them to help describe the structure of the page.

# Headers & Footers:
these elements can be used for:
         1. The main header or footer that appears at the top or
            bottom of every page on the site.
         2. A header or footer for an individual <article> or            <section> within the page. 
# Navigation(<nav>):
It used to contain the major navigational blocks on the site such as the primary site navigation.used to contain the major navigational
blocks on the site such as the primary site navigation.

# Articles:
 acts as a container for any section of a page that could stand alone and potentially be syndicated.It could be an individual article or blog entry, a comment or forum post, or any other independent piece of content, and the <article> elements can even be nested inside each
other.
# ASIDE:
IT has two purposes, depending on whether it is inside an <article>
element or not.When the <aside> element is used inside an <article>
element, it should contain information that is related to the article but not essential to its overall meaning ,and When the <aside> element is used outside of an <article> element, it acts as a container for content that is related to the entire page.
# Sections:
The (<section>) element groups related content together, and
typically each section would have its own heading.The <section> element should not be used as a wrapper for the entire page (unless the page only contains one distinct piece of content).

# Heading Groups(<hgroup>):
The purpose of the <hgroup> element is to group together a set of one or more <h1> through <h6> elements so that they are treated as one single heading.

# Figures:
It is important to note that the article should still make sense
if the content of the <figure> element were moved to another
part of the page, or even to a different page altogether.then it it should only be used when the content simply references the element and not for something that is absolutely integral to the flow of a page.It include :Images,Videos,Graphs,Diagrams,Code samples...
 
 #Process & Design :
 It discusses a process that you can use when you are creating a new
website.Every website should be designed for the target audience—not just for yourself or the site owner. It is therefore very important to
understand who your target audience is. 
    1. Why People Visit YOUR Website: Now that you know who your visitors are, you need to consider why they are coming. While
some people will simply chance across your website, most will visit for a specific reason.
    2. What Your Visitors are Trying to Achieve:It is unlikely that you will be able to list every reason why someone visits your site but you are looking for key tasks and motivations. This
information can help guide your site designs.
    3. What Information Your Visitors Need:You know who is coming to your site and why they are coming, so now you need to work out
what information they need in order to achieve their goals quickly and effectively.
    4. How Of ten People Will Visit Your Site:Some sites benefit from being updated more frequently than others. Some information (such
as news) may be constantly changing, while other content remains relatively static. 
    5. Site Maps:Now that you know what needs to appear on your site, you can start to organize the information into sections or pages.



          










