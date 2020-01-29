# Data Science Capture the Flag

What is a data science capture the flag (CTF)? To learn more checkout this blog post [link].

In short, the data science team at Duo Security created an internal training workshop to teach exploratory data analysis skills in a gamified way. In the CTF participants compete in teams to solve data analysis challenges.

The CTF sessions we led were very well received and we hope other organizations run similar exercises. To decrease the effort needed to run a data science CTF, we've open sourced much of the material we used our CTF sessions.

## Materials

There are four datasets in the following directories:

* Intro dataset
* Movie Ratings
* Jeopardy
* Challenge death

Each directory contains the data in a CSV, a README that describes the dataset, and a challenges.md with the CTF challenges and answers.

We found that participants got the most out of the session when they came prepared. There are preparation instructions in `Preparing for the CTF.md`. This leads participants to the "Tutorials" directory where there are short tutorials to help participants get familiar with data analysis environments, namely Google Sheets, Excel, or Python in a Jupyter notebook.

`Template Slides.pdf` is a a set of slides based on the presentation we make at the beginning of the session.

## Running a CTF session
Some suggested steps:

* Host a scoring platform like [CTFd](https://github.com/CTFd/CTFd) so it’s accessible by participants.
* Use our datasets and challenges to create flags. Optionally add new datasets and challenges.
* A week before the session, send out the preparation materials to participants. Prep materials are everything in this repo except for the challenge documents and the template slides.
* Start the session off with a presentation on EDA (you can base it on `Template Slides.pdf`). Let participants loose on the challenges!


## Issues/Questions
Issues should be filed using Github Issues.

## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.