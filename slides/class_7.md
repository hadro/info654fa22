This page intentionally left blank. ⬇️, ➡️, or spacebar 🛰 to start slidedeck.
---
class: center, middle

# Welcome to Class 7!

---

# Agenda

- Questions?
- News of the Week
- Readings
- Break!
- Structured Data
- XML
- JSON


---

## Assignment questions?

### Other questions?

---

## News of the Week

Drop a link on the etherpad:
<https://etherpad.wikimedia.org/p/prattsi654fa21-7>

---

# Readings

- Eric Lease Morgan. [Getting started with XML: A workshop](http://infomotions.com/musings/getting-started/getting-started.pdf) (Read Part I: "General introduction to XML") (4 min)
- 2020-02-13. Text Encoding Initiative. [A Gentle Introduction to XML](http://www.tei-c.org/release/doc/tei-p5-doc/en/html/SG.html) (60 min)
- 2005-09. Ronald Bourret. [XML and Databases](http://www.rpbourret.com/xml/XMLAndDatabases.htm) (Sections 1-4, rest is optional) (13 min)
- 2011-03-24. Matt Doyle. [JSON Basics: What You Need to Know](http://www.elated.com/articles/json-basics/) (don't worry about the JavaScript
  and PHP parts, unless you're interested!) (full text: 19 min)
- 2015-11-16. Yegor Bugayenko. [Stop Comparing JSON and XML](https://www.yegor256.com/2015/11/16/json-vs-xml.html) (5 min)
- 2018-03-28. Christine Taylor. [Structured vs. Unstructured Data](https://www.datamation.com/big-data/structured-vs-unstructured-data.html) (9 min)
- 2014-01-17. Anthony Cocciolo. [Unix Commands and Batch Processing for the Reluctant Librarian or Archivist](https://journal.code4lib.org/articles/9158) (18 min)

---
class: middle, center

# Break!

---
# Imperfect Metaphor of the Week

https://www.flickr.com/search/?q=scaffolding%20gaudi

---

# What is structured data?

--

## What are examples of unstructured data?

--

## What are examples of structured data?


---

# Why cover this?
--

We want you to be conversant in situations where structured data and exchange formats (XML, JSON, etc.) are most appropriate.

We want you to be conversant in the vocabulary of these examples, even if you don't become an expert in all the messy syntax!

Most importantly, we want you to know when you are looking at something built on top of structured data, and what the possibilities are for working with or even extending those systems.


---

# XML

---
# XML

XML is a means of sharing data between computers.

Though it is also a markup *language,* and therefore more than just a data-exchange format.

It can be read and understood by humans, but its primary purpose is to be a way of exchanging information between computers or systems.

By doing this in a structured, standardized way, it allows for data to be
passed from one system to the other without any ambiguity.

If you think of the game "Telephone" where people pass a message between each
other through whispering, it is easy to have that original message distorted
somewhere along the way. XML is a way to prevent data distortion.


---
# Three markup-related things we've seen so far this semester

- XML
- HTML
- XHTML   

--

## How would you describe the connection among these things?

--
(Also, special bonus one: anyone remember where **SGML** fits into this puzzle?)

---

Before we dive into the details of XML...
--

## What do you think are some important ways HTML and XML differ?


---
# XML

XML is a relative of HTML -- in some ways like a broader, parent markup language.

- XML is **extensible**: it does not consist of a fixed (limited) set of tags
- XML must be **well-formed** according to a defined specification
- XML documents can be **validated** against a specific schema (not just one global schema)
- XML is about the data (its contents) and not about how that data is presented

---
# XML structure

- XML must have a **declaration**
- XML can have **namespaces**
- XML has **elements** (including one and only one root element)
- XML can have **attributes**

---
# Namespaces

.center[![](./img/ns.png)]

---
# Document declaration

```xml
<?xml version="1.0" ?>
```

This is to let the software reading an XML file that you are going to present it
with XML. Computers don't always trust the file extension or other indicators
that a document is what it says it is. This says "I have prepared this XML, and
this declaration at the top of the file lets you know that XML is coming through
next."

---
# Simple Example

```xml
<?xml version="1.0" ?>
<books>
  <book>
    <title>My Father's Dragon</title>
    <author>Ruth Stiles Gannett</author>
    <subjects>
      <subject>Children's</subject>
    </subjects>
  </book>
</books>
```

---
# Example with attributes

```xml
<movies>
  <movie id="3">
    <title language="french">Jeanne Dielman, 23, Quai du Commerce, 1080 
      Bruxelles</title>
    <director nationality="belgian">Chantal Akerman</director>
  </movie>
</movies>
```

---
# How to expand?

```xml
<?xml version="1.0" ?>
<books>
  <book>
    <title>My Father's Dragon</title>
    <author>Ruth Stiles Gannett</author>
    <subjects>
      <subject>Children's</subject>
    </subjects>
  </book>
</books>
```

---
# Simple Example

```xml
<?xml version="1.0" ?>
<books>
  <book>
    <title lang="en">My Father's Dragon</title>
    <title lang="es">El Dragon de papa</title>
    <title lang="jp">エルマーの冒険</title>
    <people>
      <author>Ruth Stiles Gannett</author>
      <illustrator>Ruth Chrisman Gannett</illustrator>
    </people>
  ...
  </book>
</books>
```
---
## Let's look at a live example

--

## Simple Example

From the US Senate, which has been publishing XML for decades:

https://www.senate.gov/legislative/LIS_MEMBER/cvc_member_data.xml

(You may have to do "view source" to see the XML correctly)

---
## More complex example

Semantic markup of the Abraham Lincoln Papers collection, held by the Library of Congress:

https://findingaids.loc.gov/exist_collections/ead3master/mss/2009/ms009304.xml

(You may have to do "view source" to see the XML correctly)

---

# XML has rules

You must follow these rules when you create XML syntax:

- All XML elements must have a closing tag.
- XML tags are case sensitive.
- All XML elements must be properly nested.
- All XML documents must have a root element.
- Attribute values must always be quoted.

---
# All XML elements must have a closing tag

Not OK:
```xml
<books
<book></book>
</books>
```

---
# XML tags are case sensitive

Not OK:
```xml
<Books>
<book>
</book>
</books>
```

---
# All XML elements must be properly nested.

Not OK:
```xml
<books>
<book>
</books>
</book>
```

---
# All XML documents must have a root element

Not OK:
```xml
<?xml version="1.0" ?>
<books></books>
<books></books>
<books></books>
```
---
# Attribute values must always be quoted


Not OK:
```xml
<books>
<book id=num123>
</book>
</books>
```

---
# What if I want to use characters that are already being used?

You will have to "escape" them by using other characters that are designed to
represent what you want. Some examples:

- type <code>& amp ;</code> to display the `&` character
- type <code>& lt ;</code> to display the `<` character
- type <code>& gt ;</code> to display the `>` character
- type <code>& quot ;</code> to display the `"` character
- type <code>& apos ;</code> to display the `'` character

(Without spaces, and including the semicolon!)
---
# Where else can you find XML?

Where have you seen XML (or something likely to be XML) out in the wild?

--

XML as a way to exchange data is the foundation of several well-known file
formats:

- SVG files
- Microsoft Office files (.docx, .xlsx, and .pptx)
- RSS and Podcast feeds

---
# A note on validation

XML can be validated against its specification, to make sure it is well-formed
structured data, with no errors like described above.

But XML can also be validated against other XML files known as XSD.

XSD stands for XML Schema Definition.

These XSD
files describe the intended structure of a document -- so not only checking to
see if the metadata is well-formed, but if it adheres to more rigid standards
like the expectation of specific fields or attributes, or in a specific order.

---
# Also, DTDs

DTD stands for "Document type definition". It is another way to define a desired
XML structure, but the syntax is different from XML itself (although similar, I
guess).

A `DTD` can be seen at the top of every valid HTML page:

`<!DOCTYPE html>`

Note this is different from the XML declaration (`<?xml version="1.0"
encoding="utf-8"?>`) at the top of XML documents, and note how the structure is different.

---

# Some examples

XML is all over the place out in the wild -- a few examples!:

- [HTML5 Logo](https://upload.wikimedia.org/wikipedia/commons/6/61/HTML5_logo_and_wordmark.svg) (all SVG graphics are xml)
- Ebooks! (specifically, the .epub file format)

---

# JSON

---
# JSON

- "JavaScript Object Notation"
- a way to exchange informations (computers talking to computers)
- a standard, which means it has a [written specification](https://www.json.org/json-en.html) and rules for how it works.
- related to javascript but doesn't have to be used only with javascript

---
# Example

```json
{
  "firstName": "Josh",
  "lastName": "Hadro",
  "isAlive": true,
  "age": 100,
  "address": {
    "streetAddress": "123 Main Street",
    "city": "New York",
    "state": "NY",
    "postalCode": "10014"
  },
  "phoneNumbers": [
    {
      "type": "home",
      "number": "555 555-1234"
    },
    {
      "type": "mobile",
      "number": "123 456-7890"
    }
  ]
}
```

---
# Data types

- numbers (e.g. 1)
- strings (e.g. "Hello")
- booleans (e.g. `true`)
- no value (e.g. `null`)

---
# Data structures

- Objects in curly braces! (`{` and `}`)
  + a collection of name–value pairs 
- Arrays (things inside of `[` and `]`)
  + an ordered list of zero or more elements
- Boolean: either of the values `true` or `false`


---
# Other bits to notice

- String literals (e.g. "\"Phrase in Double Quotes, inside of Quotes\"")
- Quotation marks = strings
- Booleans are not wrapped in quotation marks
- Numbers are not wrapped in quotation marks (if they're meant as numbers)
- Elements can repeat but you must use a comma

`{ "a":123, "b":[1,2,3], "c": { "a":1, "b":2 } }`


---

# Lab Exercise time

Two options:

1. Work with Senate data in xml
2. Try an XML to JSON conversion

---
##Option 1

###Roll your own XML 

- Combine the information about the senators from your home state (or any US state!) from these two XML sources into a single, valid set of XML elements:
  - https://www.senate.gov/general/contact_information/senators_cfm.xml
  - https://www.senate.gov/legislative/LIS_MEMBER/cvc_member_data.xml

Make sure it's valid XML using a tool like this:
https://codebeautify.org/xmlvalidator

---

## Option 2
### XML --> JSON modeling

- Pick a US Senator from the [Senate committee assignments xml](https://www.senate.gov/legislative/LIS_MEMBER/cvc_member_data.xml)
- Try modeling a single `<senator>` example from that list as JSON.
  - How does nesting work in JSON?
  - How do you translate XML attributes into JSON?
- Try using a JSON validator to make sure the JSON is legal ([Example validator](https://jsonformatter.curiousconcept.com/))


---

Option 2 Senator modeling example: `XML`
```xml
<senators>
  <senator lis_member_id="S386">
  <name>
    <first>Tammy </first>
    <last>Duckworth</last>
    <suffix>        
    </suffix>
  </name>
  <party>D</party>
  <state>IL</state>
  <homeTown>Hoffman Estates</homeTown>
  <stateRank>2</stateRank>
  <bioguideId>D000622</bioguideId>
  <office>524 Hart </office>
  <committees>
    <committee code="SSEV00">Committee on Environment and Public 
      Works</committee>
    <committee code="SSSB00">Committee on Small Business and 
      Entrepreneurship</committee>
    <committee code="SSAS00">Committee on Armed Services</committee>
    <committee code="SSCM00">Committee on Commerce, Science,
     and Transportation</committee>
  </committees>
  </senator>
</senators>
```

---
**Option 2 Senator modeling example: `json`**
```json
{
   "senators":[
      {
         "senator":{
            "lis_member_id":"S386",
            "name":{
               "first":"Tammy",
               "last":"Duckworth",
               "suffix":null
            },
            "party":"D",
            "state":"IL",
            "homeTown":"Hoffman Estates",
            "stateRank":2,
            "bioguideId":"D000622",
            "office":"524 Hart",
            "committees":[
               {
                  "code":"SSEV00",
                  "committee":"Committee on Environment and Public Works"
               },
               {
                  "code":"SSSB00",
                  "committee":"Committee on Small Business and Entrepreneurship"
               },
              //Two more committees here
            ]
         }
      }
   ]
}
```
---
For comparison, most compact/compressed version of the same data: 
```json
{"senators":[{"senator":{"lis_member_id":"S386","name":{"first":"Tammy","last":
"Duckworth","suffix":null},"party":"D","state":"IL","homeTown":"Hoffman Estates"
,"stateRank":2,"bioguideId":"D000622","office":"524 Hart","committees":[{"code":
"SSEV00","committee":"Committee on Environment and Public Works"},{"code":
"SSSB00","committee":"Committee on Small Business and Entrepreneurship"},
{"code":"SSAS00","committee":"Committee on Armed Services"},{"code":"SSCM00",
"committee":"Committee on Commerce, Science, and Transportation"}]}}]}
```