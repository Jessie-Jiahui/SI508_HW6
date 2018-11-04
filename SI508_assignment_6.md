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

######################################
* **What is HTML? Describe in 1 or 2 brief sentences. (It's OK to quote something else if you want, but make sure you cite anything/anyone you quote from, and make sure you understand anyone else's words you use!)**

HTML stands fot Hypertext Markup Language, which is a standard markup language for describing things, such as title, link, image, on World Wide Web pages.


######################################
* **Why might you find an `id=` in an HTML tag? (Describe in 1 sentence.)**

id is a unique identifier (ID) specified in the html document, which could be called by its corresponding CSS and JavaScript to perform certain tasks for that unique element [1].

[1] Id. (n.d.). Retrieved from https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/id


######################################
* **Why might you find a `class=` in an HTML tag? (Describe in 1 sentence.)**

The class can be used on one or more html elements, as long as they share the same attributes, by calling the class name in its corresponding CSS and JavaScript [2].

[2] HTML | Class Attribute. (2018, September 18). Retrieved from https://www.geeksforgeeks.org/html-class-attribute/


######################################
* **What is "scraping data from websites" in a program? (It is OK to quote a source or another person, but you should cite anything/anyone else you quote here, and you should make sure you understand what you quote.)**

"Scraping data from websites" or simply "Web Scraping" is a technique employed to extract large amounts of data, instead of using the API provided by the website, but from website's explicit content. The data will be extracted and saved to a local file in a computer or to a database in table (spreadsheet) format [3]. 

[3] S. (n.d.). WebHarvy Web Scraper. Retrieved from https://www.webharvy.com/articles/what-is-web-scraping.html


######################################
* **What is happening in this line of code: `soup = BeautifulSoup('<b class="boldest">Extremely bold</b>')` ? Describe VERY briefly. Or simply answer the following question: What type is the value of `soup` after that line executes?**

a BeautifulSoup object



######################################
* **In the following code, what's any one thing that the values of `soup` and `tag_one` have in common? (note: "They're both values in Python code" is too general.)**

```py
soup = BeautifulSoup('<b class="boldest">Extremely bold</b>')
tag = soup.b
```
print(soup) >>>>> <html><body><b class="boldest">Extremely bold</b></body></html>
print(tag) >>>>> <b class="boldest">Extremely bold</b>
They both have <b class="boldest">Extremely bold</b> part. 


######################################
* **What kind of information can you find in a `BeautifulSoup Tag`'s `.attrs` attribute? e.g. if you ran the following code, what is 1 thing you might find out? (There are many possibilities, you need only answer one. But it will be useful to think about what `.attrs` is here, and whether or not you understand the following code!)** 

```py
sp = BeautifulSoup("<html><h1>Title Here</h1><a href="http://www.google.com">Link to Google...</a></html>")
print(sp.a.attrs)
print(sp.a.attrs.keys())
```

print(sp.attrs) >>>>> {'href': 'http://www.google.com'}
print(sp.attrs.keys()) >>>>> dict_keys(['href'])

.attrs attribute helps to find all the attributes of the specified tag and return them as a dictionary. And the keys() method returns a list of keys in that dictionary.


######################################
* **How are the `BeautifulSoup` methods `.find` and `.find_all` different? What does each one return? Briefly, why might you use `.find_all` instead of `.find`? (HINT: Check out the *Searching the Tree* section of the documentation...)**

The find_all() method scans the entire document, looks through a tag’s descendants and retrieves all descendants that match the filters. The find_all() returns an iterable object like this: <class 'bs4.element.ResultSet'>. If find_all() can’t find anything, it returns an empty list.

The find() method returns the first descendants that the program finds. It just returns the result, a tag object like this: <class 'bs4.element.Tag'> If find() can’t find anything, it returns None. 

If we already know that a document only have one tag we want, we can use find() method becasue it saves us time of scanning the whole document. However, if we wanna to get a list of result with the same sttribute or we are not sure if it is the only tag in a document, we should use the find_all() method to scan the entire document looking for more.



######################################
* **Is using the `BeautifulSoup` library the only way to do scraping in a Python program? If so, why is it the only way? If not, what other module options could you investigate for scraping using a Python program (list just 1 or 2)?**

	* ***Consider:* Why might you want to use `BeautifulSoup` instead of another option, even if others exist? Why might you *not* want to use `BeautifulSoup`?**


No, Python has several other options for HTML scraping in addition to BeatifulSoup, such as scrapy.

Scrapy is a rather big framework. Though it's not necessarily hard or complicated, sometimes its whole framework is not necessary to scrape some data. Compare to Scrapy, BeautifulSoup is easy and intuitive to work on [1]. Therefore, if we just want to scrape just few web page, BeautifulSoup can do a better job in terms of easy-to-use and efficiency. However, for more complicated crawls, such as lots and lots of pages, learning and using scrapy is preferred.

[1] https://www.quora.com/What-are-the-advantages-of-Scrapy-compared-to-Beautiful-Soup


######################################
* **Why is some form of caching important to perform when scraping data from web pages?**

First, caching gets rid of the waiting time for requesting data whenever developers try to test the code. In addition, caching greatly reduces the number to get access to the website, which lowers the possibility of forbidened by that website, or even related legal issues.


######################################
* **Why would you scrape data rather than using an API to get data? What's an example of a situation in which you would want or need to use scraping techniques, specifically?**

1> Wev scraping enjoys larger data availability then using API. Though most of the sites have an API today, they often apply some limitations on the data that is available through the API.
2> Wev scraping enjoys more up-to-date data. APIs tend to get updated very slowly because they are normally at the bottom of the priority list. The data served by the API may sometimes be old too. Instead, when we are scraping the content off the website, we can get what we see.
3> Wev scraping is not restrained by rate Limits. Most APIs will have their own rate limits, which reduces developers' efficiency to get those data.
4> Wev scraping often enjoys better Structure: In some cases, the data provided by API is badly structured, which turns our work to be tedious and time consuming. Developers might have to make dozens of queries before getting to the actual data that they need.

Web Scraping vs API - Web Data Extraction. (2013, December 12). Retrieved from https://www.grepsr.com/web-scraping-vs-api/
