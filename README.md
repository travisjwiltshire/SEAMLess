# SEAMLess: Seamless Environment and Methods for Interactive Lessons

The SEAMLess (Seamless Environment and Methods for Interactive Lessons) project provides a working solution and template for how courses with high levels of interactivity can incorporate in-class quizzes with visualization of results, multimodal course content (such as lecture slides, text, diagrams, videos), and coding exercises and solutions into a single, seamless interface. The project combines the R Mmarkdown format adapted for interactive tutorials (called LearnR), with an SQL database, and is deployed on a SHINY server. The online nature of this project makes is simultaenously accessible to all students during lectures without requiring any technical setup or switching between different programs, which can be a source of frustration and wasted time. Additionally, SEAMLess enables visualizing student progress during the lecture, providing a live overview of students' pace and level of understanding. 

## Minimum requirements to run the project

### For local testing:
1. RStudio and the following packages: rmarkdown, shiny, learnr

### For online deployment:
1. RStudio and the following packages: rmarkdown, shiny, learnr
2. A https://www.shinyapps.io/ account (a free account is sufficient for initial testing)
3. A web server running a database (MySQL/MariaDB)

Note that any template files including plots are made for online deployment, as the plots use anonymized data collected from students interacting with quizzes and exercises.

## Privacy

Although this project runs online, no logins are required and no identifying information is collected from the users. The only data that are saved are anonymized labels for when exercises are attempted or submitted and which answer options are selected from quizzes. These labels can not be connected to the user or their IP address in any way.
