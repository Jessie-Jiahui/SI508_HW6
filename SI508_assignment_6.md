# SI 508 - Assignment 6

### This assignment takes a somewhat different format

**You should:**

* Download this file to a directory 
* Create a Git repo inside that directory
* Make any changes necessary to files (e.g. adding answers to questions in this `SI508_assignment_6.md`)
* Add changes to git as necessary and make commits throughout the process (and look up markdown formatting if necessary)
* Create a private GitHub repository on your account called `SI508_HW6`, and make it a remote of the git repo for this assignment
* Add the instructors as collaborators to the repository so we can view it to grade ([see instructions](linktba.com))
* Make sure you've pushed all your edits to your new `SI508_HW6` GitHub repository
* Submit the GitHub repository to Gradescope -- assignment **HW6** (see the HW 6 assignment on Canvas)

* **Note** that any commits made and pushed to your repo after the deadline do *not* count for your grade (and you should not commit to the repository post-deadline pre-grading unless you are submitting the assignment late)

## Answering questions instructions

- Below, in *this* `.md` file, there are bolded questions, largely based on the documentation at this URL: `https://www.crummy.com/software/BeautifulSoup/bs4/doc/`, which is your reading for Thursday. 

* You should check out the documentation, the questions, maybe some google searches!, and perhaps try out some example code yourself, in order to be able to write answers to the questions -- which will be graded by humans. 

- You will get points for thoughtful, correct answers to each question. (Note that class meetings may be helpful for many, but likely not ALL, of these questions -- use a combination of all the info/input you have available this week, plus the internet! Note also that not all questions have *one* correct answer! There are many possible options!) Answers need not be long -- questions just need to be answered. If the answer is one word, one word is fine! No answer should be longer than a few sentences.

- Please put your answer to each question below the question, with a blank line separating your answer text from any other text. Keep the questions bolded, and do *not* make your answers bold (for easy reading by graders).

---
---

# Questions to Answer


* **What is HTML? Describe in 1 or 2 brief sentences. (It's OK to quote something else if you want, but make sure you cite anything/anyone you quote from, and make sure you understand anyone else's words you use!)**

HTML stands fot Hypertext Markup Language, which is a standard markup language for describing things, such as title, link, image, on World Wide Web pages.


* **Why might you find an `id=` in an HTML tag? (Describe in 1 sentence.)**

The id value can be used by CSS and JavaScript to perform certain tasks for a unique element with the specified id value. The id global attribute defines a unique identifier (ID) which must be unique in the whole document. Its purpose is to identify the element when linking (using a fragment identifier), scripting, or styling (with CSS).

https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/id



* **Why might you find a `class=` in an HTML tag? (Describe in 1 sentence.)**

The class is an attribute which specifies one or more class names for an HTML element. The class attribute can be used on any HTML element. The class name can be used by CSS and JavaScript to perform certain tasks for elements with the specified class name.
https://www.geeksforgeeks.org/html-class-attribute/


* **What is "scraping data from websites" in a program? (It is OK to quote a source or another person, but you should cite anything/anyone else you quote here, and you should make sure you understand what you quote.)**

Web Scraping (also termed Screen Scraping, Web Data Extraction, Web Harvesting etc.) is a technique employed to extract large amounts of data from websites whereby the data is extracted and saved to a local file in your computer or to a database in table (spreadsheet) format. ata displayed by most websites can only be viewed using a web browser. They do not offer the functionality to save a copy of this data for personal use. The only option then is to manually copy and paste the data - a very tedious job which can take many hours or sometimes days to complete. Web Scraping is the technique of automating this process, so that instead of manually copying the data from websites, the Web Scraping software will perform the same task within a fraction of the time.
https://www.webharvy.com/articles/what-is-web-scraping.html


* **What is happening in this line of code: `soup = BeautifulSoup('<b class="boldest">Extremely bold</b>')` ? Describe VERY briefly. Or simply answer the following question: What type is the value of `soup` after that line executes?**

a BeautifulSoup object


* **In the following code, what's any one thing that the values of `soup` and `tag_one` have in common? (note: "They're both values in Python code" is too general.)**

```py
soup = BeautifulSoup('<b class="boldest">Extremely bold</b>')
tag = soup.b
```

tag is a Tag object corresponds to an XML or HTML tag in the original document:


* **What kind of information can you find in a `BeautifulSoup Tag`'s `.attrs` attribute? e.g. if you ran the following code, what is 1 thing you might find out? (There are many possibilities, you need only answer one. But it will be useful to think about what `.attrs` is here, and whether or not you understand the following code!)** 

```py
sp = BeautifulSoup("<html><h1>Title Here</h1><a href="http://www.google.com">Link to Google...</a></html>")
print(sp.attrs)
print(sp.attrs.keys())
```

* **How are the `BeautifulSoup` methods `.find` and `.find_all` different? What does each one return? Briefly, why might you use `.find_all` instead of `.find`? (HINT: Check out the *Searching the Tree* section of the documentation...)**

The find_all() method looks through a tag’s descendants and retrieves all descendants that match the filters. The find_all() method scans the entire document looking for results, but sometimes you only want to find one result. If you know a document only has one <body> tag, it’s a waste of time to scan the entire document looking for more. Rather than passing in limit=1 every time you call find_all, you can use the find() method. These two lines of code are nearly equivalent: 

```py
soup.find_all('title', limit=1)
soup.find('title') 
```
The only difference is that find_all() returns a list containing the single result, and find() just returns the result.
If find_all() can’t find anything, it returns an empty list. If find() can’t find anything, it returns None


* **Is using the `BeautifulSoup` library the only way to do scraping in a Python program? If so, why is it the only way? If not, what other module options could you investigate for scraping using a Python program (list just 1 or 2)?**

	* ***Consider:* Why might you want to use `BeautifulSoup` instead of another option, even if others exist? Why might you *not* want to use `BeautifulSoup`?**

Python has several other options for HTML scraping in addition to BeatifulSoup. Here are some others:
mechanize
scrapemark
scrapy

it is easy and intuitive to work on. Scrapy is a rather big framework, it's not necessarily hard or complicated but sometimes a whole framework is not necessary to scrape some data. That's where BeautifulSoup comes in.
So if you wish to scrape just few web page you should probably stick with requests library to retrieve the pages and BeautifulSoup to parse those pages for bits of data you need.  
For more complicated crawls where you would need to crawl lots and lots of pages I would look into learning and using scrapy

https://www.quora.com/What-are-the-advantages-of-Scrapy-compared-to-Beautiful-Soup


* **Why is some form of caching important to perform when scraping data from web pages?**

I often don't want to wait a few minutes for my computer to do something it already did 10 minutes ago. In cases like this, I've found caching the results of my scraping to disk to be a useful way to avoid re-doing work.
++++++++++++++++++++++++++++++++++

* **Why would you scrape data rather than using an API to get data? What's an example of a situation in which you would want or need to use scraping techniques, specifically?**

Availability: most of the sites have an API today. Yes, they do but more often than not there are many limitations on the data that is available through the API.
Up-to-date: APIs tend to get updated very slowly because they are normally at the bottom of the priority list. The data served by the API may sometimes be old too. Instead, when you scrape the content off the website, you get what you see. You can easily verify this data.
Rate Limits: Most APIs will have their own rate limits.
Better Structure: Navigating through a badly structured API can be very tedious and time consuming. You might have to make dozens of queries before getting to the actual data that you need.

https://www.grepsr.com/web-scraping-vs-api/
