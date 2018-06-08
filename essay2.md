# Essay 2

*Andrew Walters*  
*Berkeley W241*  
*May 30, 2018*

## First Impressions

Every businessperson knows that a good first impression is valuable, but mastering the subtlety can be challenging.
Researchers at the University of Limerick, Ireland studied one such subtlety, the inclusion of an author's middle initial in an academic publication.
[Their 2014 paper](https://ulir.ul.ie/bitstream/handle/10344/5412/Igou_2014_middle.pdf?sequence=4) discovered a causal relationship between the inclusion of a middle initial in an academic publication and the reader's evaluation of the publication.
Using 85 Limerick undergraduates in randomized laboratory trials, they found that evaluations of the paper were almost a full point (out of 7) higher if the author's name included one or two middle initials.

The researchers proposed that we have been conditioned to see more formal titles in an academic setting, notably a middle initial.
Therefore the mechanism by which a middle initial causes a higher evaluation is that people associate the middle initial to an established mental pattern matching formal publications.
Patterns like this are useful at an individual level, for example any researcher who believes the thesis of this paper would be wise to include their middle initial on future publications.
There are also business applications to this insight, consider for example a content syndication company like Outbrain which recommends articles to users.
Perhaps the inclusion of a middle initial in certain contexts could drive more clicks on an article.
This begets an interesting area expansion of the original study to explore ways that online content could be modified to improve the reader experience and drive revenue.

## Further Study

The University of Limerick paper opens several possibilities for further exploration.
They specifically note that there is no effect when the middle initial is included in writing about sports or other non-academic topics.
Therefore it would be interesting to study those areas to determine what could impact people's perception of quality in the entertainment space.
Unlike the academic writing where readers are accustomed to the formal academic journal format, there are far fewer formalized conventions and institutions in writing about entertainment.
Of particular interest is online writing about entertainment, where there are far fewer institutions to help readers determine the reliability of an article.

Since the University of Limerick researchers already studied middle initials, my question revolves around the first name of the article's author.
Publishing an article under a name other than one's own is so common that there is a name for it - a pen name.
Therefore some outlets might be inclined to publish their writing with names that engender trust from their readers.
The particular first names of interest will be those that peaked in popularity at various times in the United States (statistics are available from the Social Security Administration).
The key question in our study will be whether older or younger sounding names cause the reader to trust an online entertainment article's contents.

## Experiment Setup

In order to setup this experiment, a fake online blog would be needed with only a single article designed to simulate the look and feel of typical online content.
Critically the name of the author should be displayed prominently, which is common practice in a small blog.
The article would need to present an opinion about sports, film, or music and would ideally be neutral in terms of language and tone.
If possible, a friend of the experiment team who works in media could edit the article to ensure these qualities are accomplished.
At the bottom of the article would be buttons that allow the reader to rank the trustworthiness of the article on a numerical scale, which will be our outcome measurement.

In addition to the trustworthiness measurement, we might also wish to capture a few covariates.
Assuming that this experiment is going to be conducted virtually (as opposed to in-person) then we would want to collect a subject token, which would be distributed to them before they read the article.
This would accomplish a couple of things, first and foremost ensuring that nobody could vote more than once.
This would also measure our non-response bias, represented by unused tokens.
We could also use the token to track personal information about the user, although if we're using a service like mechanical turk then our only information would be the service used.
We might also wish to measure the time a user spends on the page before they vote, to ensure they actually read the article.

The site will be entirely static content with the exception of the voting mechanism and the name of the blog.
We will create 7 treatment groups, with each treatment group representing a decade from 1950 to 2010.
Every group will be a treatment group, since there is no "real" name for the author of the article for a control group.
The first name on the title of the blog will be a name that was (1) one of the 20 most popular names during a birth year in that decade and (2) peaked in popularity only during that decade.
For each decade a handful of names may fit the criteria and all will be used.
When a new user visits the site, they will receive a web page a randomly selected name from a randomly selected treatment group and their vote will be recorded.

It will likely be necessary to run a trial phase of this experiment to ensure the test site is operational and intuitive for the experiment subjects.
The trial phase will not necessitate random sampling and can be simply friends and family of the researchers.

## Experiment Subjects

In an ideal experiment, we make a random selection of our population of interest for each treatment group.
In this case the population we are studying is people who live in the United States and would read an online article about entertainment.
We could reach this population by running online ads, but there would be a couple of issues.
First is just the cost of running search ads to direct random users to our page, but there are also concerns about non-response bias and reaching the entire population instead of just people who search for related terms.

A more practical experiment would require us to make some compromises.
A possible source of readers for the article is an human task assignment system like mechanical turk, which would eliminate the non-response bias but would not fully cover our population.
Since not every person who reads online entertainment content works with mechanical turk, we cannot possibly reach every person we are interested in.
For budgetary reasons this might have to be close enough to our population in order to collect responses, although we will need to take care to ensure that readers are from the US.
Using a service like this makes the experiment execution fairly simple, as we just need to pay an appropriate number of people to read the article and record their responses.
If a large enough number of responses can be collected, there is potential to re-run this experiment with different articles on different subjects.

## Experiment Analysis

There will be two steps to the data analysis: (1) cleaning the data to eliminate erroneous responses and (2) testing for the significance of responses.
Step 1 can be accomplished using the covariates collected alongside the measurement variable.
For example, any repeated subject tokens or small time spent on page measurements can be discarded.
Step 2 is slightly more complicated than a standard treatment-control experiment since there is no control group.
Logically there is no such thing as a "control first name" so instead we will be analyzing the 7 treatment groups as 7 independent experiments.
In each of these experiments, the treatment (in this case the decade of the names' popularity) will be compared to the control measurement of every name outside the treatment group.
For each "experiment" the average treatment effect will be computed along with the statistical significance against the sharp null hypothesis and the corresponding confidence interval.

## Conclusion

The issue of trust in online publishing is of particular interest in the "fake news" era.
Determining the subtle subtle ways in which a platform can engender trust in it's readers is a topic of concern for businesses and the public.
If a causal link can show that certain names are more trustworthy in a particular domain, then we could expect online publishers to use that tactic to influence opinions to a greater degree.
Hopefully as we learn more about the psychology surrounding the way people interact with online content, we can develop better ways to identify and overcome our subtle biases.
