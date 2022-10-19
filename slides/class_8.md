This page intentionally left blank. ⬇️, ➡️, or spacebar 🛰 to start slidedeck.
---
class: center, middle

# Welcome to Class 8!

---

# Agenda

- Questions?
- Next assignments
- News of the Week
- Readings
- Break!
- APIs
- Linked Data
- API activities


---
class: middle, center

## Questions?

---

# Blank Technology Canvas Assignment

Moving this back a week

---

## News of the Week

Drop a link in the airtable via the etherpad:  
- <https://etherpad.wikimedia.org/p/prattsi654fa22-8>  
- <https://airtable.com/shrU21jPMI0cEPvw4>

---
# Readings


- 2015-02-05. Dorothea Salo. [MARC, Linked Data, and Human-Computer Asymmetry](https://dsalo.info/marc-linked-data-and-human-computer-asymmetry/) (7min)
- 2015-02-19. Matthew Hughes. [What Is An API & What Are They Good For?](http://www.makeuseof.com/tag/api-good-technology-explained/) (6 min)
- 2020-12-13 Raivat Shah. [Introduction to REST APIs: Get started with RESTful APIs using a real-world example](https://towardsdatascience.com/introduction-to-rest-apis-90b5d9676004) (5 min)
- Current. White House. [WhiteHouse api-standards](https://github.com/WhiteHouse/api-standards)
- 2012-06-16. Manu Sporny. [What is Linked Data?](http://www.youtube.com/watch?v=4x_xzT5eF5Q) (video, 12 minutes)
- 2017-05-07. Jonathan Blaney. [Introduction to the Principles of Linked Open Data](https://programminghistorian.org/en/lessons/intro-to-linked-data) (25 minutes)
- 2017-10-19. Mia Ridge. [Unlocking Potential: Where Next for Open Cultural Data in Museums?](http://museum-id.com/unlocking-potential-next-open-cultural-data-museums-mia-ridge/) (7 min)

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
class: middle, center

# Break!

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

# Activity: TV Maze API

Let's try to answer the question:   
**"How do I find out which episodes of my favorite show have the shortest and longest runtimes (lengths)?* (*Using only API calls, and not the web-rendered version of the TV Maze site)"**

Let's use the TV Maze API Documentation to help us:
<https://www.tvmaze.com/api>

A hint: 
- The first API call you'll need is this one, which takes a keyword parameter -- replace "SHOW" with all or part of the title for your favorite show: <https://api.tvmaze.com/search/shows?q=SHOW>

Also, if you're using Chrome, you'll probably want to install this JSON formatter to help you read the API responses more easily:
<https://chrome.google.com/webstore/detail/jsonvue/chklaanhfefbnpoihckbnefhakgolnmc?hl=en>

So, what bit of information from that first API call could we use to plug into another one of the API calls in [the documentation](https://www.tvmaze.com/api) that would give us a list of all episodes from a given show?

Give this a try and play with the API endpoints and read the documentation for a few minutes before moving to the next slide. 

---
# TV Maze API

Answer: You'll need the `show.id`!

Where can this be found in the [search API response](https://api.tvmaze.com/search/shows?q=She%20Hulk)?

```json
[
   {
      "score":0.770629,
      "show":{
         "id":43517,
         "url":"https://www.tvmaze.com/shows/43517/she-hulk-attorney-at-law",
         "name":"She-Hulk: Attorney at Law",
         "type":"Scripted",
         "language":"English",
         "genres":[
            "Comedy",
            "Science-Fiction"
            //
```

In this example searching for the "She Hulk" show, what we need is the third line there, where it says `"id":43517`.

Now that you've found the equivalent for your favorite show, where can we plug in the `show.id` to get information about all episodes for a show?

---
# TV Maze API

There are multiple ways to do this! But the simplest is probably the [`Episode List` endpoint](https://www.tvmaze.com/api#show-episode-list).

Can you figure out how to combine the `show.id` you got from the previous call with this example URL from the documentation to get the list of all episodes?

<https://api.tvmaze.com/shows/:id/episodes>

--

For the She Hulk show, which has an `id` of 43517, it would look like this:

<https://api.tvmaze.com/shows/43517/episodes>

What parts of the response to that contains the information we seek?

---

# TV Maze API

```json
[
   {
      "id":2354151,
      "url":"https://www.tvmaze.com/episodes/2354151/she-hulk-attorney-at-law-1x01-a-normal-amount-of-rage",
      "name":"A Normal Amount of Rage",
      "season":1,
      "number":1,
      "type":"regular",
      "airdate":"2022-08-18",
      "airtime":"",
      "airstamp":"2022-08-18T12:00:00+00:00",
      "runtime":38,
      "rating":{
         "average":7.4
      },
      //
```

---

# TV Maze API

The `"runtime"` key is the datapoint we're interested in. There's one `"runtime"` value for each JSON object (each object == one show episode).

If a show only has a few episodes, like this She Hulk example, it's relatively easy enough to scan the list visually to see what the shortest and longest runtimes might be.

Next questions to ponder and work through:
- How would answer the shortest/longest episode question if there are huge number of episodes?
- How would you use the same set of APIs to answer the following questions:  
    - How many total episodes does your favorite show have?
    - How many total episodes aired during just the first season of your favorite show?
    - How would we find out the name of your favorite show in other languages?


---
# Activity: Wordnik API

- [https://developer.wordnik.com/docs](https://developer.wordnik.com/docs)

This API documentation comes with examples and a way to test out the API in the
browser.


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


