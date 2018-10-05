# HIV-Newspaprer-Articles-Clustering
using data scraped from The Hindu and Times of Indai from 2001 to 2018 for temporal and geographical analysis as well as labelling of the data into several clusters in python using Geotext and NLTK

BY CHINMAY SINGH
2ND YEAR UNDERGRAUDTE STUDENT
DEPARTMENT OF CHEMICAL ENGINEERING
IIT KHARAGPUR



HIV ATRICLES CATEGORIZATION
USING ARTICLES FROM THE HINDU AND THE TIMES OF INDIA (2001 TO 2018)
INDTRODUCTION
The aim was to make clusters/categorize the articles that have been published in the Indian English newspapers from 2001 to 2018 on Human Immunodeficiency Virus (HIV). The findings generate an insight into the topic and helps frame better strategy to curb HIV.
Approach Used
i.	Web spider was deployed to the websites of these Newspapers with the help of Scrapy library in python. This provided and output of the articles with time stamps and titles as separate columns.
ii.	The data obtained was fed into a model made on the model of the Agile Model
iii.	The missing values were imputed and the date was converted to date format of pandas library.
iv.	The Natural Language Text Corpora (NLTK) was used to tokenize(break up into words) and for the stemming of the word (linguistic normalization)
v.	The stop words and punctuations were accounted for and removed using NLTK stop words.
vi.	The word to vector approach was used to convert all the preprocessed words into vectors with the help of a shallow two layer neural network.
vii.	For Clustering an ensemble of Density – Based Spatial Clustering of Applications with Noise(DBSCAN) (since it does not require input of number of clusters),
 Agglomerative Hierarchical Clustering(provides option to choose number of clusters) and K Nearest Neighbors (KNN)(using distance measured with cosine similarity) was used for performing the grouping of the articles.
viii.	Multi Dimensional Scaling(MDS) was used for dimensionality reduction( gives more precision and faster runtime.
ix.	The model fit and used for prediction on the data.
x.	The output was analyzed and clustering was labelled
xi.	Important parameters like Geo-tagging of the articles was done using libraries like GeoText.
xii.	The seaborn library was used to perform temporal and geographical analysis of the data.
INFERENCES

 

MULTIDIMENSIONALLY SCALED MODEL
( CLUSTERS OVERLAPPING BECAUSE OF LARGE NUMBER OF DIMENSIONS )
NUMBER OF ARTICLES PUBLISHED YEAR WISE
NUMBER OF MENTIONS OF MAJOR COUNTRIES IN THE ARTICLES
	 

IN	LK	US	TR	PK	ZA	CN	PH	CZ	GB	TH	PL
2628	3	338	112	73	44	43	190	107	112	31	61



 
 
MENTION OF VARIOUS MAJOR CITIES

FREQUENCY OF OCCURRENCE OF VARIOUS TYPES OF ARTICLES

A	311
B	104
C	953
D	87
E	185
F	223
G	284


Cluster Name	Type of Article
A	Statistics relating to HIV
B	Aricles Relating to Government/Individual Decisions on HIV related issues
C	Spreading Stigma On HIV
D	News Informing of Positive Developments against HIV(non scientific)
E	News informing about HIV test methods And previous diagnosis results
F	Articles spreading awareness
G	News Informing of Positive Developments against HIV(scientific)
 
Clustered CSV output file(with A,B,C,D,E,F  replaced by 0,1,2,3,4,5,6 respectively) 

WAY FORWARD


THE ANALYSIS CAN BE USED TO IDENTIFY THE CURRENT PROBLEM WITH THE HIV ERADICATION PROGRAMME. IT CAN ALSO BE USED TO IDENTIFY THE PRINCIPAL AFFECTED AREAS. THE REPORT CAN ALSO BE USED AS A INDICATOR OF THE AWARENESS DRIVE OF THE SOCIAL BODIES AND TO MEASURE AS WELL AS ENHANCE THEIR EFFICIENCIES


