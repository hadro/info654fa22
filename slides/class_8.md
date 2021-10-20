This page intentionally left blank. ⬇️, ➡️, or spacebar 🛰 to start slidedeck.
---
class: center, middle

# Welcome to Class 8!

---

# Agenda

- Questions?
- News of the Week
- Readings
- Break!
- APIs
- Linked Data
- Break!
- API work


---
class: middle, center

## Questions?

---

# Blank Technology Canvas Assignment

Two components:

- [Pitch presentation](https://hadro.github.io/info654fa21/assignments/blank_technology_presentation.html) (short, 5-7 minutes, due November 10)
- [Final narrative report](https://hadro.github.io/info654fa21/assignments/blank_technology_canvas_report.html) (a few components, to be turned in as a website, due December 15)

---

## News of the Week

Drop a link on the etherpad:
<https://etherpad.wikimedia.org/p/prattsi654fa21-8>

---
# Readings


- 2015-02-05. Dorothea Salo. [MARC, Linked Data, and Human-Computer Asymmetry](https://dsalo.info/marc-linked-data-and-human-computer-asymmetry/) (7min)
- 2015-02-19. Matthew Hughes. [What Is An API & What Are They Good For?](http://www.makeuseof.com/tag/api-good-technology-explained/) (6 min)
- 2020-12-13 Raivat Shah. [Introduction to REST APIs: Get started with RESTful APIs using a real-world example](https://towardsdatascience.com/introduction-to-rest-apis-90b5d9676004) (5 min)
- Current. White House. [WhiteHouse api-standards](https://github.com/WhiteHouse/api-standards)
- 2012-06-16. Manu Sporny. [What is Linked Data?](http://www.youtube.com/watch?v=4x_xzT5eF5Q) (video, 12 minutes)
- 2016-03-20. Ruth Kitchin Tillman. [An Introduction to RDF for Librarians (of a Metadata Bent)](http://ruthtillman.com/introduction-rdf-librarians-metadata/) (24 min)
- 2017-10-19. Mia Ridge. [Unlocking Potential: Where Next for Open Cultural Data in Museums?](http://museum-id.com/unlocking-potential-next-open-cultural-data-museums-mia-ridge/) (7 min)


---
class: middle, center

# Break!

---
Let's start here: 

--
# TIERS OF DATA ACCESS

--
- **Static data**: HTML, XML, flat files, CSV, etc.  

--
- **Flowing data**: via APIs, via http, read and write access  

--
- **Meaningful data**: Linked Data, semantically linked, machine and human readable  



---
class: center, middle

# APIs

---
# APIs

### Application
### Programming
### Interface

.right[![](img/calm-waters.gif)]

---
# What is an API?

.center[![](img/cowboy_on_computer.gif)]

---
# Computers talking to computers

.center[![](img/computer_e-mail.gif)]

- Rules around how computers communicate
- Used as a framework for many computer things! Like for your computer to talk
to your printer.
- In modern-casual terms: Rules for how you can retrieve data from websites 🤖

.center[![](img/computer_e-mail.gif)]

---
# Computers talking to computers

So APIs are all about computers talking to computers, but they're also an
*abstraction layer* that allows people to easily understand how to get the data
that they need from a computer.

When you query an API (asking it to give you some data), it will always return
data in a specific format. The data itself might change, but the arrangement of
the data will always be the same.

.center[![](img/computerhorsepics.gif)]

<!-- ---
# What is an API? (video version)

<iframe width="560" height="315" src="https://www.youtube.com/embed/ecT42O6I_WI"
frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> -->

---
# key-value pairs

Like a lot of computer concepts, APIs are composed of *properties and values*

---

## Where have you encountered APIs?

What comes to mind when you think of APIs?  
In what contexts have you heard the term?  
What do people do with these?  

---

# What kinds of APIs would you like to see?

If you could get access to any kind of data in a structured way, what kinds of things would be among your top choices?


---
# Aside: Why are most APIs closed? 

Most APIs with lots of data require you to register, often asking you to sign up for what's called a "developer key" or "access token" or something similar. 

--
## Why? 

What are the various reasons for this?

---

## An open API playground: IIIF Image API

<https://www.learniiif.org/image-api/playground>

Try the following:
- change "size" to `pct:10` [this means 10% of the original size]
- change "Region" to `full`
- change "Region" to `square`
- Now, refresh the page
- change the third number in "Region" from `799` to `1400`, so the whole string reads `1015,1460,1400,824`
- change "size" to `600,` [don't forget the comma after the 600]
- Now copy the `Requested image url:` just above the image, and paste it into a new tab
- Now try any of the above transformations by editing the URL directly!

---

# Let's build a GovTrack API query!

- <http://www.govtrack.us/api/v2/role>

--

What data is this API call returning? What do we see? How could we refine it? 

--

- <http://www.govtrack.us/api/v2/role?state=ny>

--
- <http://www.govtrack.us/api/v2/role?state=ny&current=true>  

--
- <https://www.govtrack.us/api/v2/role?state=ny&current=true&role_type=senator> 

--
- <https://www.govtrack.us/api/v2/role?state=ny&current=true&role_type=senator&format=xml>

---

# Linked Data

Sir Tim Berners Lee, from earlier in this semester: 

“We haven’t got data on the web as data.” 

"Documents you read – that’s it.”

“Data – you can do all kinds of stuff with it.”

---

# FIVE STAR DATA

<https://5stardata.info/en/>

1. Open License
2. Structured data
3. Open format
4. Use URIs
5. Get useful data back!


---

## Three Rules: 

1. HTTP names -- not just documents, but for things the documents are about.
2. Get important information back
3. Define relationships


---

## It's all about relationships

Often called TRIPLES

**SUBJECT, OBJECT, PREDICATE**

--

Josh, IIIF, is employee of  
Josh, Rhea, is the parent of  
Josh, Andrew, is the sibling of  

--

IIIF, Josh, is employer of  
Rhea, Josh, is the child of  
Andrew, Josh, is the sibling of 

--

Now, to make this proper Linked Data, you must use URIs for each element of the triple.

---
# Linked Jazz

An example:

Linked Jazz relationships (an amazing Pratt project!)

https://linkedjazz.org/api/relationships/all/nt

Three entries:

```
<http://dbpedia.org/resource/Roy_Haynes> <http://purl.org/vocab/relationship/knowsOf> 
<http://dbpedia.org/resource/Charles_Mingus> .

<http://dbpedia.org/resource/Roy_Haynes> <http://purl.org/ontology/mo/collaborated_with> 
<http://dbpedia.org/resource/Charles_Mingus> .

<http://dbpedia.org/resource/Dave_Brubeck> <http://purl.org/vocab/relationship/knowsOf> 
<http://dbpedia.org/resource/Charles_Mingus>

```


---
# Questions



---
# Activity: The New York Times API

- [https://developer.nytimes.com/apis](https://developer.nytimes.com/apis)

This API documentation comes with examples and a way to test out the API in the
browser.

---
# Getting started steps

Follow the steps on this page:
<https://developer.nytimes.com/get-started>

1. Sign up
2. Register an App
3. Add the Books API (and others, if you want) to your App
4. Return to the APIs page and select the Books API

---
# Activity 2: Wordnik API

- [https://developer.wordnik.com/docs](https://developer.wordnik.com/docs)

This API documentation comes with examples and a way to test out the API in the
browser.

---