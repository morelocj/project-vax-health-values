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

But that is not what this project is about. Anyway, here as in elsewhere, the data from REDCap came out with text as the values for variables. In order to prep the data for easy analysis, I needed to recode everything I wanted to use into integer variables as opposed to string/object variables. This applied to almost every variable in the dataset that I wanted to use. Of particualr importance, scales that combined multiple survey items could not be calculated until each off the applicable survey items was converted into numerical data. 

Once everything was converted to numerical values, I used the Sklearn module to do a Nearest Neighbors imputation to take care of missing values (MAR). Some of the variables I used for this were ordinal, and with these, the imputation results something came back with numbers that included fractions/decimals. In these cases, I rounded the imputed values toward their nearest whole number. 

I ran a table of correlations on the continuous variables, and have put some of them in scatterplots, like the following examples:

![image](https://user-images.githubusercontent.com/8931602/236530708-998df5e5-09be-4850-9642-a78e8f40b312.png)

![image](https://user-images.githubusercontent.com/8931602/236531056-3fcb6bb4-750a-4026-aba5-899a4cab034f.png)

![image](https://user-images.githubusercontent.com/8931602/236531450-e1056a8b-64ef-4e57-82d0-efc6aed420ac.png)

This last of the 3 charts is especially interesting to me because of the way the spread varies.
Without getting too into analyzing the meaning of these, for now I will just note that there is a lot that can be done with this data, via exploration, and I will continue to play around with it. 
