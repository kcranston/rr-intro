Reproducible Science Workshop - Intro II
========================================================
font-family: 'Helvetica'
date: May 14, 2015

Intro I summary
========================================================

* We learned that everyone struggles with reproducibility and that it is a hindrance to moving science forward

* We focused on 4 problems: organization, documentation, automation, and dissemination with a fairly simple analysis. Over the two day workshop, data analysis tasks will become more complex as we gather more data and ask more complicated questions

Four facets
========================================================

* Organization: you will be given tools to organize your projects so that you don't have a single folder with hundreds of files

* Documentation: you will learn the difference between binary files (e.g. docx) and text, files and why text files are preferred for documentation using a simple tool called markdown that you can use to write descriptions of your data and your workflow so that anyone can pick up your data and follow what you are doing

* Automation: you will learn about the power of scripting in the R programming language and how you can integrate that into markdown to create automated data analyses

* Dissemination: you will see that publishing is not the end of your analysis, rather it is a way station towards your future research and the future research of others

Toolkit
========================================================

![R](img/Rlogo-1.png)

* * * 

![RStudio](img/RStudio-Logo-Blue-Gradient.png)

Why R?
========================================================

* Programming language for data analysis
* Free!
* Open source
* Widely used and supported across all disciplines
* Can be used on Windows, Mac OS X, or Linux

* * * 

![RSplashScreen](img/RSplashScreen.png)

Why not language X?
========================================================

* There are a number of other great programming tools out there that can also be used to improve the reproducibility of your analysis

* The key is to use some type of language that will allow you to automate and document your analysis

* Once you master one language you'll probably find it easier to learn another

Why RStudio?
========================================================

* Gives you a single environment to combine your documentation and your analysis with markdown support
* Runs on top of R
* Gives you a bunch of really cool features that we'll explore throughout the workshop

* * * 

![RSplashScreen](img/RStudioSplash.png)

Anatomy of RStudio
========================================================

<center>
![RSplashScreen](img/RStudioSplash.png)
</center>


Anatomy of RStudio
========================================================
* Upper right: workspace and a history of the commands that you've previously entered

* Lower right: Any plots that you generate + access to files, help, packages

* Left: Console
    * Every time you launch RStudio, it will have the same text at the top of the console telling you the version of R that you’re running. 
    * Below that information is the prompt. 

Revisit Exercise 1 
========================================================

* Open `intro-01-template.Rmd` 
* Click on *Knit HTML* to compile the document

Goals of the next exercise
========================================================

* Demonstrate "good practice" for organizing data files and analysis documents (R markdown)
* How to read data from a file
* How to combine data from multiple data frames
* How to subset data
* How to make simple plots in ggplot

**NOT** about understanding all the R commands, but **rather** getting the big picture of how using R in this way facilitates reproducible analyses

Exercise 2: Extending your analysis
========================================================

1. Append the new data `gapminder-7080.csv` and `gapminder-90plus.csv` to your existing data set. <br>*Be careful* as you do so, as the ordering of columns in the data set may not match between the different CSV files!

2. Create line plots of life expectancy over time for Canada, Mexico, and the United States that run from 1952 to 2007.<br>
*Stretch goal:* In the same plot, add similar line plots for Cambodia, China, and Japan and Uganda, Egypt, and South Africa.

3. Create a scatter plot depictcting GDP vs. life expectancy of countries in Europe for 2007. <br>
*Stretch goal:* In the same plot, add another scatter of points for Asia, Africa, and the Americas, coloring the countries from each region (continent) with the same color.

Exercise 2: Resources
========================================================

* Open `intro-02-template.Rmd` 
* Click on *Knit HTML* to compile the document

Exercise 2: Take aways
========================================================

* The analysis is self-documenting
* It's easy to extend or refine analyses by copying and modifying code blocks
* The results of the analysis can be disseminated by sending Markdown and providing data sources, or just simply providing the generated HTML of just a summary of the analysis is needed

Reproducibility checklist
========================================================

* Serves as a tool to help you think about the reproducibility of your data analysis
* Many of the questions can be thought of as having a yes/no answer
* A better approach would be to see the questions as being open ended with the real question being, "What can I do to improve the status of my project on this bullet point?"
* With that in mind, you'll never get 100% of the bullets right for your project, but you'll always be improving

RC: Documentation (1/2)
========================================================

* Is there a README file that indicates the purpose of the project, who to contact with questions, a map of the directory structure, and a description of what software and hardware is needed to reproduce your workflow?
* Are there README files in each folder describing the contents of the folder, how they were acquired/generated?
* Is there a CITATION file that tells users how to site the project, data, and code?
* Are there instructions on how to obtain the raw data and citations for those data?
* Is there a list of dependencies with the exact version number of every external application used in the process?
* Do you indicate dates that websites were accessed to obtain data?

RC: Documentation (2/2)
========================================================
* Are there appropriate LICENSE files that specify the license under which you're distributing your content, data, and code? Have you edited them to include info pertinent to your project?
* Have you noted the license(s) for others peoples' content, data, and code used in your analysis?
* For analyses that utilize a random number generator, have you noted the underlying random seed(s)? Do you state the other seeds that you have tested the results with?
* Is your code well documented?
* Do you use a self-commenting coding practice?
* Do each of your scripts have a header indicating the inputs, outputs, and dependencies?
* Is it documented how files relate to each other?

RC: Organization (1/2)
========================================================

* Are all data, code, results, and documentation housed within a monophyletic folder structure?
* Is this folder structure under version control?
* Is the project's repository publicly avaialable?
* Are there assurances that this repository will remain accessible?
* Is your project folder structured to separate your data, code, documentation, and results?
* Does your code run from the project's home directory and output to the appropriate directory?

RC: Organization (2/2)
========================================================
* Are your raw and processed data files separated?
* Is your raw data truly raw or has it been manipulated?
* Are files that store manually-entered data structured to be easily read by a computer?
* Do files use a consistent naming scheme that indicates what they contain?
* Is there a mechanism in place to archive large files?
* When using other people's data, are you defensive against tarbombs?

RC: Automation (1/2)
========================================================

* Is the project under the control of a makefile? Could one run `make clean; make`?
* How long would it take to rebuild your directory system if your hard drive failed?
* Is manual manipulation of data kept to a minimum?
* If manual manipulation is required, is there sufficient documentation to re-do the manipulation
* Does data processing make use of open software code

RC: Automation (2/2)
========================================================

* How sensitive are results to differences in operating system, dependency versions?
* Is code written to be flexible enough to the addition of new data?
* Does code include unit tests to confirm that it does what you think it does?
* Does your repository make use of continuous integration tools to insure internal reproduciblity?

RC: Publication
========================================================

* Are papers and reports from the project generated using literate programming tools so that results are not hard-coded?
* Did you include a reproducibility statement or declaration at the end of your paper(s)?
* Did you archive preprints of resulting papers in a public repository?
* Did you release the underlying code and new data at the time of submitting a paper?
* What mechanisms are in place to insure your project remain accessible and reproducible in 5 years?
