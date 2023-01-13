# SEAMLess: Seamless Environment and Methods for Interactive Lessons

The SEAMLess (Seamless Environment and Methods for Interactive Lessons) project provides a working solution and template for how courses with high levels of interactivity can incorporate in-class quizzes with visualization of results, multimodal course content (such as lecture slides, text, diagrams, videos), and coding exercises and solutions into a single, seamless interface. The project combines the R Mmarkdown format adapted for interactive tutorials (called LearnR), with an SQL database, and is deployed on a SHINY server. The online nature of this project makes is simultaenously accessible to all students during lectures without requiring any technical setup or switching between different programs, which can be a source of frustration and wasted time. Additionally, SEAMLess enables visualizing student progress during the lecture, providing a live overview of the students' pace and level of understanding. 

## Privacy

Although this project runs online, no logins are required and no identifying information is collected from the users. The only data that are saved are anonymized labels for when exercises are attempted or submitted and which answer options are selected from quizzes. These labels can not be connected to the user or their IP address in any way.

## Minimum requirements to run the project

### For local use:
1. RStudio and the following packages: rmarkdown, shiny, learnr

### For online deployment with visualizations of student progress and quiz answers:
1. RStudio and the following packages: rmarkdown, shiny, learnr
2. A https://www.shinyapps.io/ account (a free account is sufficient for initial testing)
3. A web server running a database (MySQL/MariaDB)

### For online deployment without progress tracking or an overview of quiz answers:
1. RStudio and the following packages: rmarkdown, shiny, learnr
2. A https://www.shinyapps.io/ account (a free account is sufficient for initial testing)

Note that any template files including plots are made for online deployment, as the plots use anonymized data collected from students interacting with quizzes and exercises.

## Instructions

### For local use:

To run a template intended for local testing [Quizzes without plots](https://github.com/travisjwiltshire/SEAMLess/tree/main/Templates/Quizzes%20without%20plots), download the folder and open the .Rmd file in RStudio. Ensure you have installed the required packages (rmarkdown, shiny, learnr), you can do this with `install.packages("package_name")` if needed.

You should see a green arrow with the text "Run Document" above the code window. A local version of the file will be compiled and it will open in a new window. This may take a few minutes. What you will see is an accurate and interactive representation of what would be deployed online. You will also have the option to open it in a browser to see what it would look like to students interacting with it on the web. Alternatively, you can provide the students with the .rmd files to run locally.

