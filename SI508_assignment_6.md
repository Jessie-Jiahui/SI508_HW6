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

* **Why might you find an `id=` in an HTML tag? (Describe in 1 sentence.)**




* **Why might you find a `class=` in an HTML tag? (Describe in 1 sentence.)**



* **What is "scraping data from websites" in a program? (It is OK to quote a source or another person, but you should cite anything/anyone else you quote here, and you should make sure you understand what you quote.)**




* **What is happening in this line of code: `soup = BeautifulSoup('<b class="boldest">Extremely bold</b>')` ? Describe VERY briefly. Or simply answer the following question: What type is the value of `soup` after that line executes?**




* **In the following code, what's any one thing that the values of `soup` and `tag_one` have in common? (note: "They're both values in Python code" is too general.)**

```py
soup = BeautifulSoup('<b class="boldest">Extremely bold</b>')
tag = soup.b
```



* **What kind of information can you find in a `BeautifulSoup Tag`'s `.attrs` attribute? e.g. if you ran the following code, what is 1 thing you might find out? (There are many possibilities, you need only answer one. But it will be useful to think about what `.attrs` is here, and whether or not you understand the following code!)** 

```py
sp = BeautifulSoup("<html><h1>Title Here</h1><a href="http://www.google.com">Link to Google...</a></html>")
print(sp.attrs)
print(sp.attrs.keys())
```

* **How are the `BeautifulSoup` methods `.find` and `.find_all` different? What does each one return? Briefly, why might you use `.find_all` instead of `.find`? (HINT: Check out the *Searching the Tree* section of the documentation...)**




* **Is using the `BeautifulSoup` library the only way to do scraping in a Python program? If so, why is it the only way? If not, what other module options could you investigate for scraping using a Python program (list just 1 or 2)?**

	* ***Consider:* Why might you want to use `BeautifulSoup` instead of another option, even if others exist? Why might you *not* want to use `BeautifulSoup`?**


* **Why is some form of caching important to perform when scraping data from web pages?**


* **Why would you scrape data rather than using an API to get data? What's an example of a situation in which you would want or need to use scraping techniques, specifically?**
