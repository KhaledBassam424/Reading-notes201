# Who want to learn how to design and build websites from scratch
Anyone who has a website and want to make it better(that may be built using a content management system, blogging software or an e-commerce platform) and wants more control over the appearance of their pages The only things you need in order to use this book are a computer with a web browser and a text editor(such as Notepad, which comes with Windows, or TextEdit, which comes with Macs).

To explain the pages will come next ahead in the book you are reading here is some definitions to help you :

Introduction: pages come at the beginning of each chapter. They introduce the key topics you will learn about.

Reference pages : introduce key pieces of HTML & CSS code. The HTML code is shown in blue and CSS code is shown in pink.

Background pages appear on white; they explain the context of the topics covered that are discussed in each chapter.

Diagram and infographics pages: are shown on a dark background. They provide a simple, visual reference to topics discussed.

Example pages: put together the topics you have learned and demonstrate how they can be applied in each.

Summary pages: come at the end of each chapter. They remind you of the key topics that were covered in each chapter.

At work, when people look at the Programmer screen and see it full of code, it’s not unusual to get a comment about it looking very complicated or how clever he must
be to understand it. The truth is, it’s not that hard to learn how to write web pages and read the code used to create them; you certainly don’t have to be a “programmer.”
Understanding HTML and CSS can help anyone who works with the web; designers can create more attractive and usable sites, website editors can create better content
marketers can communicate with their audience more effectively, and managers can commission better sites and get the best out of their teams.
The Structure of This Book :

1: HTML : stands for Hyper Text Markup Language. HTML is the standard markup language for creating Web pages one of the core technologies for building Web pages.
2: CSS : Cascading Style Sheets one of the core technologies for building Web pages.
3: Practical : We end up with some helpful information that will assist you in building better websites, We look at some new tags that will be introduced in HTML5 to help describe the structure of your pages.
we end up looking at topics that will help you once you have built your site, such as putting it on the web, search engine optimisation (SEO) and using analytics software to track who comes to your site and what they are looking at.
How People Access the Web: Before we look at the code used to build websites it is important to consider the different ways in which people access the web and clarify someterminology:
1: Browsers : People access websites using software called a web browser. Popular examples include Firefox, Internet Explorer, Safari, Chrome, and Opera.
2: Web Servers : When you ask your browser for a web page, the request is sent across the Internet to a special computer known as a web server which hosts the website.Web #### servers are special computers that are constantly
connected to the Internet, and are optimized to send web pages out to people who request them.
3: Screen readers :Screen readers are programs that read out the contents of a computer screen to a user. They are commonly used by people with visual impairments.
4:Devices: People are accessing websites on an increasing range of devices including desktop computers, laptops, tablets, and mobile phones. It is important to
remember that various devices have different screen sizes and some have faster connections to the web than others.
How Websites Are Created: All websites use HTML and CSS, but content management systems blogging software, and e-commerce platforms often add a few more technologies into the mix.
How the Web Works: When you visit a website, the web server hosting that site could be anywhere in the
world. In order for you to find the location of the web server, your browser will first connect to a Domain Name System (DNS) server.
Structure
We come across all kinds of documents every day of our lives. Newspapers, insurance forms, shop catalogues ,the list goes on.

In this chapter you will:
See how HTML describes the structure of a web page and Learn how tags or elements are added to your document , Write your first web page.
**How Pages Use Structure: Think about the stories you read in a newspaper: for each story, there will be a headline, some text, and possibly some images ,The structure is very similar when a news story is viewed online (although it may also feature audio or video). This is illustrated on the right with a copy of a newspaper alongside the corresponding article on its website.

HTML Describes the Structure of Pages : The HTML code is made up of characters that live inside angled brackets these are called HTML elements. Elements are usually
made up of two tags: an opening tag and a closing tag. (The closing tag has an extra forward slash in it.) Each HTML element tells the browser something about the information that sits between its opening and closing tags.
HTML Uses Elements to Describe the Structure of Pages and Tags act like containers, They tell you something about the information that lies between their opening and closing tags.
Attributes Tell Us More About Elements :Attributes provide additional information about the contents of an element.
They appear on the opening tag of the element and are made up of two parts: a name and a value, separated by an equals sign.
Body, Head & Title:
<body> You met the <body> element in the first example we created. Everything inside this element is shown inside the main browser window.
<head> Before the <body> element you will often see a <head> element. This contains information about the page (rather than information that is shown within
the main part of the browser window that is highlighted in blue on the opposite page). You will usually find a
or on the tab for that page (if your browser uses tabs to allow you to view multiple pages at the same time).
**let me guide you throght steps to Creating a Web Page on a PC: To create your first web page on a PC, start up Notepad. You can find this by going to: Start All Programs (or Programs) Accessories Notepad You might also like to download a free editor called Notepad++ from notepad-plus-plus.org. Go to the File menu and select Save as… You will need to save the file somewhere you can remember. Save this file as test.html

**Looking at How Other sites are Built you can do that buy opening the page you want to look at and Once you have opened this page, you can look for the View menu in your browser, and select the option that says Source or View source.

In end of theis chapter Here is some of the thinge you know about now: HTML pages are text documents. HTML uses tags (characters that sit inside angled brackets) to give the information they surround special meaning. Tags are often referred to as elements. Tags usually come in pairs. The opening tag denotes the start of a piece of content; the closing tag denotes the end. Opening tags can carry attributes, which tell us more about the content of that element. Attributes require a name and a value. To learn HTML you need to know what tags are available for you to use, what they do, and where they can go.

The Evolution of HTML:
HTML 4 Released 1997
XHTML 1.0 Released 2000
HTML5 Released 2000
DOCTYPEs:Because there have beenseveral versions of HTML, each web page should begin with a DOCTYPE declaration to tell a browser which version of HTML the page is using (althoughbrowsers usually display the page even if it is not included). We will therefore be including one in each example for the rest of the book.

**There is a way to wright Comments in HTML :

**ID Attribute: Every HTML element can carry the id attribute. It is used to uniquely identify that element from other elements on the page. The id attribute is known as a global attribute because it can be used on any element.

**Class Attribute: Its value should describe the class it belongs to. In the example on the left, key paragraphs have a class attribute whose value is important. The class attribute on any element can share the same value. So, in this example, the value of important could be used on headings and links, too.

**Block Elements: Some elements will always appear to start on a new line in the browser window. These are known as block level elements.

Inline Elements: Some elements will always appear to continue on the same line as their neighbouring elements. These are known as inline elements.

Grouping Text &Elements In a Block:

* : element allows you to group a set of elements together in one block-level box. * : The element acts like an inline equivalent of the
element. It is used to either: 1. Contain a section of text where there is no other suitable element to differentiate it from its surrounding text 2. Contain a number of inline elements. The most common reason why people use elements is so that they can control the appearance of the content of these elements using CSS *
