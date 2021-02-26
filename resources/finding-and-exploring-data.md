TODO:
- Research for data verkennen op bronnen en tips
- Tools installeren
- Tutorial voor elke tool zoeken
- Boeken zoeken
- Verschil tussen proof/reference/source and a data source. A reference you found supporting a claim you make is not a data source. If your project makes the claim that mental health has declined and you reference an article that describes a 40% increase in new patients for psychiatrists, that is not a data source, simply a reference. If the article includes a graph that shows the increase, that's also not a data source. The data behind that graph is, however. Make a clear difference in your work between sources you use and actual data you use. 

# Finding and Exploring Data

This guide is meant to help you get started on finding data and exploring patterns within it. It's definitely not a conclusive guide. If you're looking for something more complete, check out the books mentioned at the end of the guide.

I'll cover part of this guide in a video which will be shared by Frank and Maaike. The guide may be updated and extended with new resources later.

## Types of data
There are many different types of data. In this section I'm not taling about the nature of the data or even its contents, I'm just focusing on the differences in how you as an interpretor have to deal with data. This depends mostly on the origin and format of the data.

- Data in visualizations in articles/papers/books: Data is often visualized in articles and other story formats. If the article is any good, the original source of data can be linked. You should always check out the original source and try to reach your own conclusions from the source when possible. If you end up copying anything straight from an article, always mention the article as the source (and the original source of the data if possible)
- Data in an interactive visualization: These days much of the data you see has already been visualized in a way that helps you understand patterns and allows you to explore the data visually. As with static visualizations in articles, always remember you are seeing a certain view of the data that was designed with a certain purpose. It may be misleading. Often, the original data source will be linked. [This live Corona tracker map](https://gisanddata.maps.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6) is a good example. It shows the original sources at the bottom.
- Raw data: When you get to the original raw data you basically have a file or a set of files. On the one hand it means you'll have to do more work to understand the data but on the other hand it also means you get the data in its purest form. You have all the freedom to explore and analyze it. In the exploration section I'll show you how to do that.
- Metadata: This is a special kind of data that describes something else. For instance, the filetype of a dataset, the number of entries in the dataset, the age of all people described in a dataset, the collectors of the data etc. Metadata helps you understand data. Raw data can not be interpreted without metadata. If all you have is a file of numbers, there's no way to understand what that data is about.
- Data gathered by you: In the CCDL project you're very much encouraged to gather data yourself, whether it be qualitative or quantitative. This is especially powerful if you can get other group members to gather the same data in a different location so you can actually make your work cross-cultural. Think long and hard about the format of the data you want to collect. Make sure all collectors have the same understanding of the data to be collected. Use well-chosen and understood variable names for your data and be sure to collect metadata as well. If you ask people in the street what hobbies they've picked up to help them survive the Covid lockdown, be sure to collect the metadata of how old they are for instance, as that could later be relevant in understanding differences in your dataset and the datadet collected by someone else. In general, the more metadata you collect, the better. You never know what you might need later and it's often impossible to go back and collect the metadata you need.

The rest of this guide will focus on working with raw data. Data in articles and interactive visualizations has already been turned into 'information' which you can process by understanding the visualization.

## Data sources
- [Google dataset search](https://datasetsearch.research.google.com/): Very powerful dataset search tool powered by google.
- [Kaggle](https://www.kaggle.com/): Great source for raw datasets on virtually any topic.
- [Public datasets](https://github.com/awesomedata/awesome-public-datasets): An up-to-date list of links to datasets spanning a wide array of topics
- Governmental sources: usually quite reliable although that depends on the reliability of the government in question, the data collectors, and the topic of the data. Governments usually have a lot of data about health of citizens.
- API's: API's are services offered to programmers. They're set up to answer specific questions like "Give me all cars of brand X and production year Y". API's need to be queried using code.

## Data formats
Data can have many different shapes and forms, here I'll cover a *few* common formats you can encounter in the wild.

- Tabular data: `.csv, .xls, .tsv` Is data where each datapoint is separated by a special character. This type of data can be imported into programmes like  Excel (windows), Numbers (mac), or Google Sheets (web).
- Data used by software/programmers: `.json, .xml` This type of data is used by programmers and imported using code. Sometimes they can be converted into tabular data using tools or websites.
- Geospatial data: `shapefile, esri grid, geoJSON` This data always references locations. It can be imported into programmes like QGIS and be used to create maps for instance.
- Proprietary data: `.xls, .spss, .dta` These formats are designed to be used by a specific programme. In this case, Excel, SPSS, Stata. Sometimes they can also be opened in other programmes or converted to more accessable formats.
- Databases: `SQL, RDF, DB` These formats contain a database and can only be used with a database system compatible with that format. 

[Here is an article](https://guides.library.oregonstate.edu/research-data-services/data-management-types-formats) on data formats. If you don't find the format you're looking for explained here, try googling the format or file extension (for instance '.xml format'). 

### Converting data formats
Formats are designed to make the structure of data predictable by formulating a set of rules the data must adhere to. For instance, in a `.csv` file all datapoints must be separated (delimited) by a comma. 
Because it is in a predictable format it can in theory be transformed into another format as along as the rules can still be applied. As most of you don't have a background in data science, I would suggest that if you find anything you cannot open with a tabular data programme like Excel, you try to change it into a format that can. In general, anything you can convert to CSV you will be able to work with.
To convert data formats, try googling "format to format" for instance "json to csv". If you get stuck, ask a question in Slack.

## Data exploration
Mental proces(https://datahero.com/blog/2013/11/20/5-beginners-steps-to-investigating-your-dataset/)
Snifftest: https://www.youtube.com/watch?v=OIafM8pGbfQ&ab_channel=KnightCenterCourses
https://journalismcourses.org/course/data-visualization-for-storytelling-and-discovery/


### Using tools
- Excel
- Tableau
- QGis (for GIS data)
- R (mss bij code)

### Using code
- Javascript: 
    + [D3.js](https://d3js.org/): amazing for cleaning, transforming, exploring and visualizing data
    + [Chart.js](https://www.chartjs.org/): chart generator which does a lot of work for you
- Python
    + [https://realpython.com/pandas-python-explore-dataset/](Pandas): I'm not experienced with exploring data using Python myself but my 🐍 friends tell me you will probably use Pandas and Numpy.



## More about data exploration
- links
- to 
- other 
- resources
- 