This page intentionally left blank. ⬇️, ➡️, or spacebar 🛰 to start slidedeck.
---
class: center, middle

# Welcome to Class 5!

---

# Agenda

- Questions from last week?
- News of the Week
- Readings
- Break!
- Web wrap-up
- Files, files, files!
- BREAK!
- Website project breakout groups



---

## Assignment questions?

### Other questions?

---

## News of the Week

Drop a link on the etherpad:
<https://etherpad.wikimedia.org/p/prattsi654fa21-5>

---

# Readings

- We have slides for these
- Let's step through each of them and discuss
---
# Readings -- some notes

## Cobweb
  - [Internet Archive's Wayback Machine](https://web.archive.org/)
  - [perma.cc](https://perma.cc/)
  - version control
  - robots.txt
  - (Internet Archive has [changed its mind](https://blog.archive.org/2017/04/17/robots-txt-meant-for-search-engines-dont-work-well-for-web-archives/) about that)

---
# Readings -- some notes

## The House Archives Built
- "Archives and The Archives"
- Contrasting the "digitize everything and sort it later" mentality, very prevalent whenever Internet Archive comes up
- Some context: ["More Product, Less Process"](https://en.wikipedia.org/wiki/More_Product,_Less_Process)
- "the language serves the systems, not the subjects."
- "When archives feel stymied by standards and best practices, digitization can feel liberatory."

---
# Readings -- some notes

## Bodleian and UCLA
  - Digitization seems simple, but there are tons of decisions and editorial calls made in terms of how to represent something
  - [Laurie Spiegal](https://en.wikipedia.org/wiki/Laurie_Spiegel)
  - [Part 1](https://youtu.be/TzOJtZYsGSA?t=226) - explaining digital vs analog
  - [Part 2](https://www.youtube.com/watch?v=oconRQBZff0) - "how does the computer help you save time?"
  - a lot of technical jargon: Aja, Blackmagic, XLR, TBC, etc
  - workflow diagrams!
  - reliance on old hardware

---
# Readings -- some notes

 - [h264 really is magic!](https://sidbala.com/h-264-is-magic/)
 - and the [JPEG playground article](https://parametric.press/issue-01/unraveling-the-jpeg/) -- again with the standards!
 - For another, deeper look: Amy Wibowo -- [Glitching hour](https://www.thestrangeloop.com/2018/the-glitching-hour.html) toy
 - rgb vs YCbCr, how do our eyes work?
   + PS this is one of the underrated, genius innovations of the 20th century


---
class: center, middle

# Web wrap-up

- What questions do you have about web tech?

---
# Compression

  - images, video, and audio, text
  - Compacting of bits in order to streamline file size
  
--
- **Lossless vs. Lossy**

--
  - can see it on the web, like a bootstrap.min.js file
    + [bootstrap-alert.js](https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/2.3.1/js/bootstrap-alert.js), vs
    + [bootstrap-alert.min.js](https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/2.3.1/js/bootstrap-alert.min.js)
    + These files contain the same information!
  - can see it when images look bad

---

 ![pixel loss](https://upload.wikimedia.org/wikipedia/commons/e/e9/Felis_silvestris_silvestris_small_gradual_decrease_of_quality.png)

---
# Generation loss

<iframe width="560" height="315" src="https://www.youtube.com/embed/DYvNsiJwldg" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

"What happens when you have two VCRs, two VHS cassettes, and plenty of time on your hands?"

---
class: middle

# .center[💻 File Formats 💻]

---
# Let's talk about files

- What is a file?
- What is a file format?
- Magic numbers
- File structures
- Standardization
- Registries

---
# Files

Things that can be
- Open
- Read 
- Changed
- Closed
- Permissions modified

---
# File Formats

We have many different types of files! These are categorized into different formats, with different ways to determine what to do with the data inside the file.

---
# Magic numbers

What separates a file from the rest of the binary landscape?
### Magic numbers!
Magic numbers are sometimes known as file signatures. They are a short string of hexadecimal code that  allow a file to identify itself as a certain type of file.

---
# File structure

- Magic numbers (file signature)
- Header
- Body (or payload)

---
# File standardization

- Outlines all the rules required to follow to have a valid file
- Can be standardized through a standards body (but not required)
- Can be open (anyone can read) or closed (proprietary, only people in a company/organization can access)

---
# Standardization example

A great resource for explaining how a file format is made, by Ross Spencer:
[http://exponentialdecay.co.uk/blog/genesis-of-a-file-format/](http://exponentialdecay.co.uk/blog/genesis-of-a-file-format/)

---
# Learning about file formats

- [ArchiveTeam's File Format Wiki](http://fileformats.archiveteam.org)

---
# Registries 

- [PRONOM](http://www.nationalarchives.gov.uk/PRONOM/Default.aspx) (UK National Archives)
- [Format Descriptions](https://www.loc.gov/preservation/digital/formats/fdd/browse_list.shtml) (US Library of Congress)
- [`file`](https://en.wikipedia.org/wiki/File_(command) (Unix command)
- [File Formats Wiki](http://fileformats.archiveteam.org/wiki/Main_Page) (ArchiveTeam)

---
# Images

## JPEG
- came around in the 90s, varying degrees of Compression, very popular

## GIF
- pronounce as you like, not good quality but it can loop
- have become videos now on the web, including giphy.com!

## PNG
- lossless compression, which means its bigger. not very web-optimized but higher quality.
- it also has another layer, transparency!

---
# Images, cont

## SVG
- XML for images
- this is vector-based instead of pixel-based
- Illustrator instead of Photoshop 
- we can view source on this https://www.w3.org/html/logo/downloads/HTML5_Logo.svg
- raster vs vector https://upload.wikimedia.org/wikipedia/commons/6/6b/Bitmap_VS_SVG.svg

## Other formats...
- Webp, BMP, TIFF, JPEG2000, RAW

---

## Audio

- WAV (regular, LPCM, BWF)
- limited to 4GB, very high quality stream though
- FLAC

## Video
- containers and codecs (same for audio)

---
class: middle, center

# Questions?

---
# Wrap-Up HTML Lab 

Let's use the remaining time to do breakout groups again, and continue working on the elements in the lab from last week: 
- Slides starting from last week here: <https://hadro.github.io/info654fa21/slides/class_4.html#40>


- [Glitch](https://glitch.com/edit/#!/chrome-fantastic-blue?path=style.css%3A1%3A0) (Click "Remix to Edit")
- [Repl.it](https://replit.com/@hadro/654-04-fall-2021#index.html) (Click "Fork" to edit, though you'll have to create an account)
- [codepen.io](https://codepen.io/pen/) (Copy the HTML from one of the examples above to paste into this option)

If you feel comfortable with the steps there, consider using the time to work on a general template for the pages on the Personal Homepage assigment



