# SEAMLess: Seamless Environment and Methods for Interactive Lessons

The SEAMLess (Seamless Environment and Methods for Interactive Lessons) project provides a working solution and template for how courses with high levels of interactivity can incorporate in-class quizzes with visualization of results, multimodal course content (such as lecture slides, text, diagrams, videos), and coding exercises and solutions into a single, seamless interface. The project combines the R Mmarkdown format adapted for interactive tutorials (called LearnR), with an SQL database, and is deployed on a SHINY server. The online nature of this project makes is simultaenously accessible to all students during lectures without requiring any technical setup or switching between different programs, which can be a source of frustration and wasted time. Additionally, SEAMLess enables visualizing student progress during the lecture, providing a live overview of the students' pace and level of understanding. 

An example of what the project looks like when deployed can be seen here: https://travisjwiltshire.shinyapps.io/lecture10.

## Privacy

Although this project runs online, no logins are required and no identifying information is collected from the users. The only data that are saved are anonymized labels for when exercises are attempted or submitted and which answer options are selected from quizzes. These labels can not be connected to the user or their IP address in any way.

## Minimum requirements to run the project

### For local use:
1. RStudio and the following packages: rmarkdown, shiny, learnr

### For online deployment without progress tracking or an overview of quiz answers:
1. RStudio and the following packages: rmarkdown, shiny, learnr
2. A https://www.shinyapps.io/ account (a free account is sufficient for initial testing)

### For online deployment with visualizations of student progress and quiz answers:
1. RStudio and the following packages: rmarkdown, shiny, learnr
2. A https://www.shinyapps.io/ account (a free account is sufficient for initial testing)
3. A web server running a database (MySQL/MariaDB)

Note that any template files including plots are made for online deployment, as the plots use anonymized data collected from students interacting with quizzes and exercises.

## Instructions

### For local use:

To run a template intended for local testing ([Quizzes without plots](https://github.com/travisjwiltshire/SEAMLess/tree/main/Templates/Quizzes%20without%20plots) for example), download the folder and open the .Rmd file in RStudio. Ensure you have installed the required packages (rmarkdown, shiny, learnr), you can do this with `install.packages("package_name")` if needed.

You should see a green arrow with the text "Run Document" above the code window. A local version of the file will be compiled and it will open in a new window. This may take a few minutes. What you will see is an accurate and interactive representation of what would be deployed online. You will also have the option to open it in a browser to see what it would look like to students interacting with it on the web. Alternatively, you can provide the students with the .Rmd files to run locally.

### For online deployment without progress tracking or an overview of quiz answers:

First, you will need to create an account on https://www.shinyapps.io/. You can start with a free account for testing purposes, individual use or use within a smaller team, but if you anticipate higher usage levels (e.g. regular use by students during lectures or at home) you will most likely need to switch to a paid subscription. Usage is counted per hour of the application being actively used and this is multiplied when more users are running the application simultaenously. The free tier comes with 25 hours per month and there are 4 paid tiers to choose from to increase the number of hours.

After setting up an account, you will need to connect your RStudio and ShinyApps.io account. For this, go to RStudio and navigate to Tools -> Global Options -> Publishing -> Publishing Accounts -> Connect ... -> ShinyApps.io. Follow the instructions provided in this window to get your token from https://www.shinyapps.io/ and connect the account.

Once the initial setup is complete, publishing is quite straightforward. Run the document as instructed in the local use section ([Quizzes without plots](https://github.com/travisjwiltshire/SEAMLess/tree/main/Templates/Quizzes%20without%20plots) is an easy example that does not require a database server) and you will see a blue "Publish" button at the top right of the window, press this and select the files you wish to publish. This should include the .Rmd file and any other files/folders used in the .Rmd (e.g. data, images). After a few minutes, the files will be deployed and you will see the url at the bottom of the "Deploy" console in RStudio.

### For online deployment without progress tracking or an overview of quiz answers:

In addition to the steps above, you will need to set up a web server hosting a database (MySQL or MariaDB). This will be used to store answers from students to quizzes and progress labels for exercises, which will then be used to generate plots to visualize student involvement in the lecture. For this project, the minimal option from [Hostnet](https://www.hostnet.nl/vps) for a virtual private server was used but any equivalent server will work. Follow the instructions in the [database setup guide](https://github.com/travisjwiltshire/SEAMLess/blob/main/Documentation/Database%20setup.pdf) for initial setup.

Once the databse is running and some initial tables have been created, you can test it with the template files that include different options for visualizing quiz anwers and exercise progress found [here](https://github.com/travisjwiltshire/SEAMLess/tree/main/Templates/Quizzes%20with%20plots). You will need to fill in your database IP address and login information in the beginning of the document (instructions are provided in comments). After that, publishing and testing work the same as described in the abvove sections.

### For creating interactive lectures:

Fruther instructions for creating interactive lectures with RMarkdown and LearnR can be found [here](https://github.com/travisjwiltshire/SEAMLess/blob/main/Documentation/).

You may also find the following resources helpful:
- [Documentation for R/RStudio](https://www.rdocumentation.org/)
- [Educational tools using R/RStudio](https://education.rstudio.com/teach/tools/)
- [A quick start guidue for RMarkdown]( https://rmarkdown.rstudio.com/lesson-1.html)
- [Documentation for RMarkdown](https://rmarkdown.rstudio.com/docs/)
- [A quick start guide for LearnR](https://rstudio.github.io/learnr/articles/learnr.html)
- [Documentation for LearnR](https://rstudio.github.io/learnr/articles/learnr.html)
- [Documentation for ShinyApps](https://docs.posit.co/shinyapps.io/)

## Funding

This project was partially supported by Tilburg University's EDUiLAB (Educational Innovation Lab): Innovation your education program awarded to Travis J. Wiltshire and funding from the Tilburg University School of Humanites and Digital Sciences.  
