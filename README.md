# project-vax-health-values
This repo contains an exploration of the dataset I got from first survey I sent out during my postdoc research at the William F. Connell School of Nursing at Boston College. I built the survey on REDCap, once my research proposal was accepted by the Boston College IRB. I sent the survey out over Facebook, via a paid advertising campaign, in September, 2021. I obtained 575 usable responses. 
Initially, I cleaned and analyzed the data using SPSS and Stata, and after a variety of tests and explorations, I came out with two different multiple regression analyses that I sent out in the form of journal articles with the help of a couple of co-authors. The articles are currently under review.
I also decided to reclean and reanalyze the data using Python/Pandas/Matplotlib via VS Code, and Tableau, not for journal article publishing purposes, but for more general dissemination and descriptive analysis, i.e. on GitHub, on Tableau Public, and in blog posts.
The following is a brief description of my process using Python, and my code is contained in the various pages of this repo. 

Returning to the raw, deidentified data downloaded from REDCap, I revisited my demographic control variables, testing them for normality, kurtosis, and so on, when continuous. Here are a few charts from this exploration:
![image](https://user-images.githubusercontent.com/8931602/236516822-b8c262c3-815b-4244-b910-297158887ce7.png)
The age variable is bimodal. This variable has more missing values than any other demographic variable.
![image](https://user-images.githubusercontent.com/8931602/236517050-568d8fdf-3bbf-49f6-adbd-2702ab4bb1aa.png)
The income variable (household monthly income) is certainly not even across categories - the middle economic categories have the greatest frequency.
![image](https://user-images.githubusercontent.com/8931602/236517670-b4301192-df40-4e1a-b3c0-4cf5ae3992d3.png)
It is interesting to consider income in reference to subjective class identification.


