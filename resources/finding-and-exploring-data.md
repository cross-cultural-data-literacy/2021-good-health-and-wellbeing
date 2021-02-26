# Finding and Exploring Data
![Image of a person embarking on data exploration](../images/data_exploration.png)

_source:<span>Photo by <a href="https://unsplash.com/@itssammoqadam?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Sam Moqadam</a> on <a href="https://unsplash.com/s/photos/relations-data?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText">Unsplash</a></span>_

This guide is meant to help you get started on finding data and exploring patterns within it. It's definitely not a conclusive guide. If you're looking for something more complete, check out the books mentioned at the end of the guide.

I'll cover part of this guide in a video which will be shared by Frank and Maaike. The guide may be updated and extended with new resources later. Some terms commonly used in data exploration are _italicized_ and are worth learning about separately.

## Sources of data
There are many different types of data. In this section I'm not talking about the nature of the data or even its contents, I'm just focusing on the differences in how you as an interpretor have to deal with data. This depends mostly on the origin and format of the data.

### Difference between a source and a data source
A reference you found supporting a claim you make is **not** a data source. If your project makes the claim that mental health has declined and you reference an article that describes a 40% increase in new patients for psychiatrists, that is not a data source, simply a reference. If the article includes a graph that shows the increase, that's also not a data source. The data behind that graph is, however. Make a clear difference in your work between sources you use and actual data you use. When we talk about data in this guide, we mean data as a collection of datapoints.

- Data in visualizations in articles/papers/books: Data is often visualized in articles and other story formats. If the article is any good, the original source of data can be linked. You should always check out the original source and try to reach your own conclusions from the source when possible. If you end up copying anything straight from an article, always mention the article as the source (and the original source of the data if possible)
- Data in an interactive visualization: These days much of the data you see has already been visualized in a way that helps you understand patterns and allows you to explore the data visually. As with static visualizations in articles, always remember you are seeing a certain view of the data that was designed with a certain purpose. It may be misleading. Often, the original data source will be linked. [This live Corona tracker map](https://gisanddata.maps.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6) is a good example. It shows the original sources at the bottom.
- Raw data: When you get to the original raw data you basically have a file or a set of files. On the one hand it means you'll have to do more work to understand the data but on the other hand it also means you get the data in its purest form. You have all the freedom to explore and analyze it. In the exploration section I'll show you how to do that.
- Metadata: This is a special kind of data that describes something else. For instance, the file type of a dataset, the number of entries in the dataset, the age of all people described in a dataset, the collectors of the data etc. _Metadata_ helps you understand data. Raw data can not be interpreted without metadata. If all you have is a file of numbers, there's no way to understand what that data is about.
- Data gathered by you: In the CCDL project you're very much encouraged to gather data yourself, whether it be qualitative or quantitative. This is especially powerful if you can get other group members to gather the same data in a different location so you can actually make your work cross-cultural. Think long and hard about the format of the data you want to collect. Make sure all collectors have the same understanding of the data to be collected. Use well-chosen and understood variable names for your data and be sure to collect metadata as well. If you ask people in the street what hobbies they've picked up to help them survive the Covid lockdown, be sure to collect the metadata of how old they are for instance, as that could later be relevant in understanding differences in your dataset and the dataset collected by someone else. In general, the more metadata you collect, the better. You never know what you might need later and it's often impossible to go back and collect the metadata you need.

The rest of this guide will focus on working with raw data. Data in articles and interactive visualizations has already been turned into 'information' which you can process by understanding the visualization.

## Finding Data
- [Google dataset search](https://datasetsearch.research.google.com/): Very powerful dataset search tool powered by google.
- [Kaggle](https://www.kaggle.com/): Great source for raw datasets on virtually any topic.
- [Public datasets](https://github.com/awesomedata/awesome-public-datasets): An up-to-date list of links to datasets spanning a wide array of topics
- Governmental sources: usually quite reliable although that depends on the reliability of the government in question, the data collectors, and the topic of the data. Governments usually have a lot of data about health of citizens.
- API's: API's are services offered to programmers. They're set up to answer specific questions like "Give me all cars of brand X and production year Y". API's need to be queried using code.
- Scientific data: Scientific articles often link to the data used in the research described. You can find these articles using tools like [google scholar](https://scholar.google.com/)

## Data formats
Data can have many different shapes and forms, here I'll cover a *few* common formats you can encounter in the wild.

- Tabular data: `.csv, .xls, .tsv` Is data where each datapoint is separated by a special character. This type of data can be imported into programs like  Excel (windows), Numbers (mac), or Google Sheets (web).
- Data used by software/programmers: `.json, .xml` This type of data is used by programmers and imported using code. Sometimes they can be converted into tabular data using tools or websites.
- Geospatial data: `shapefile, esri grid, geoJSON` This data always references locations. It can be imported into programs like QGIS and be used to create maps for instance.
- Proprietary data: `.xls, .spss, .dta` These formats are designed to be used by a specific program. In this case, Excel, SPSS, Stata. Sometimes they can also be opened in other programs or converted to more accessible formats.
- Databases: `SQL, RDF, DB` These formats contain a database and can only be used with a database system compatible with that format. 

[Here is an article](https://guides.library.oregonstate.edu/research-data-services/data-management-types-formats) on data formats. If you don't find the format you're looking for explained here, try googling the format or file extension (for instance '.xml format'). 

### Converting data formats
Formats are designed to make the structure of data predictable by formulating a set of rules the data must adhere to. For instance, in a `.csv` file all datapoints must be separated (delimited) by a comma. 
Because it is in a predictable format it can in theory be transformed into another format as along as the rules can still be applied. As most of you don't have a background in data science, I would suggest that if you find anything you cannot open with a tabular data program like Excel, you try to change it into a format that can. In general, anything you can convert to CSV you will be able to work with.
To convert data formats, try googling "format to format" for instance "json to csv". If you get stuck, ask a question in Slack.

## Data exploration
If you want to use data in your project, you'll need to make sense of it first. Data can be turned into information when you understand what the data means. The next step is to present it to other people in a way they can understand but that is outside the scope of this guide.
Understanding data is a complex mental process. It starts with metadata like: 
- Who created the data and why?
- What is the subject of the data?
- What does each variable in your data describe for instance
    + Time, location, amount
    + 14:48; 36.9, -4.8; 28000
- Is the data representative? If it's data about a population, are all people represented equally in the dataset? Are certain groups missing or underrepresented? What does that mean for the validity of the data?

When you understand the metadata you have, you can start to explore the data. By asking yourself questions about it like "are there differences between datapoints collected during the week versus during the weekend?" You will start to see patterns in the data which will trigger new questions to be answered. Read [this article](https://datahero.com/blog/2013/11/20/5-beginners-steps-to-investigating-your-dataset/) to understand more about the mental process you go through while exploring data.

### Understanding each variable
You can start by scrolling through a _column_ to get an idea of the content of that column. It often makes sense to order the column and see what the highest and lowest values represent. Often it's also useful to look at the average value and the standard deviation from that value. If you have a statistical background you can look into other [descriptive statistics](https://conjointly.com/kb/descriptive-statistics/). This is also the best time to look for obvious mistakes or _errors_ in the data and _missing values_. You can also make data more readable by telling excel all values in a column are of a certain _data type_ like date, number or text. [Here's a great guide on understanding and cleaning up data in individual columns](https://www.youtube.com/watch?v=OIafM8pGbfQ&ab_channel=KnightCenterCourseshttps%3A%2F%2Fjournalismcourses.org%2Fcourse%2Fdata-visualization-for-storytelling-and-discovery%2F).

### Understanding a datapoint
When you understand what individual columns mean, a crucial step is to understand individual datapoints. This step is often overlooked and possibly the most crucial in understanding the subjects of the data. In the video linked above, the data is about real people. You can't fully understand what one value in one column means without knowing more about the subject. A common misconception is that data is objective, data doesn't lie. This is wrong for many reasons and you can only ever hope to get closer to the truth about your subject through data.
Try to understand what the data can tell you about a few individual datapoints by reading the _values_ in each column for one row of data. Think about what this dataset can and **can't** tell you about its subjects. You may start to see some patterns in the data already when looking at the similarities and differences between datapoints.

### Understanding patterns
Start by writing down expectations you have about the data. For instance: I expect more customers visit the shop right after 17:00 because that's when people get out of work. These expectations can relate to one ore more columns. Here is an expectation related to at least two columns: I expect people with higher income to travel more often. 
Looking for patterns in your data and understanding them is an art of its own. Here are some great starters on the subject. (@maaike) 

### Visualizing data
Some patterns only become visible when you visualize data. For instance by making a linechart of temperatures over time. Many tools have built-in visualization features that help you create different types of _graphs_.

### Using tools
You can read through raw data using any text editor but most datasets are simply to large to understand in this manner. Here are some tools to help you out, ordered by ease of use.

#### Excel (windows), Numbers (mac), Google Sheets (web)
Excel (and its Mac and Web based alternatives) is the most common tool used in exploring data. Some file types can be opened straight away with excel and some may need to be [imported](https://support.microsoft.com/en-us/office/import-or-export-text-txt-or-csv-files-5250ac4c-663c-47ce-937b-339e391393ba). If you do this correctly, each column should represent a different variable in your dataset and each row should represent one datapoint.

One powerful (and slightly more advanced) feature that allows you to find _correlations_ between different variables is _pivot tables_. Using them you can quickly throw variables into a table to see how they relate. This is how to use pivot tables in [Excel](https://www.youtube.com/watch?v=qu-AK0Hv0b4&ab_channel=CodyBaldwin), [Numbers](https://macmost.com/simulating-pivot-tables-in-numbers.html), and [Google Sheets](https://support.google.com/docs/answer/1272900?co=GENIE.Platform%3DDesktop&hl=en).

#### Tableau
[Tableau](https://www.tableau.com/) is a great way to visualize data which can be an important step in understanding it. It's **not free** but you can use a trial.

#### SPSS, Stata
These are programs designed for statistical analysis. Takes a bit of practice to understand and use them well as they are meant to be used by researchers.

#### QGIS (for GIS data)
[QGIS](https://www.qgis.org/en/site/), an awesome _open source_ tool for working with geospatial (location) data. Using QGIS you can quickly import different data layers on a map and get geospatial insights.

### Using code
If you know how to code, you can import, clean, manipulate, transform, analyze and visualize data all by yourself! It takes a lot of work to understand how to do this but it does allow for the most control over your data. If you don't know how to code yet, be aware it takes serious time to learn.

#### Javascript
- [D3.js](https://d3js.org/): amazing for cleaning, transforming, exploring and visualizing data. I can highly recommend [this free course on data visualization with D3 by Curran Kelleher](https://curran.github.io/dataviz-course-2018/).
- [Chart.js](https://www.chartjs.org/): chart generator which does a lot of work for you in visualizing data.

#### Python
- [https://realpython.com/pandas-python-explore-dataset/](Pandas): I'm not experienced with exploring data using Python myself but my 🐍 friends tell me you will probably use Pandas and Numpy.

#### R
- R is used a lot in data science. [Here's an open source online book](https://r4ds.had.co.nz/index.html) about how to use it.

#### Artificial Intelligence
AI can be a very powerful tool to find patterns in data. In the past couple years, software has become available that makes it possible for people who are not schooled in AI to use AI through visual interfaces to explore data. If this is completely new to you, it's probably a bit much to dive into during the CCDL project. If you want to try it anyway, send me a message on Slack to help get you started.

## More about data exploration
- [Basic intro into understanding data](https://towardsdatascience.com/what-is-data-8f94ae3a56b4)
- [Course on Data Visualization for Storytelling and Discovery by Alberto Cairo](https://journalismcourses.org/course/data-visualization-for-storytelling-and-discovery/)
- [Book on data visualization by Andy Kirk](https://www.amazon.com/Data-Visualisation-Handbook-Driven-Design/dp/1473912148)