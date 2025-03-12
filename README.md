# Bangkok-AirBnb-Recommender-System-Content-Filtering-
### **Project Objective** 
Design a recommender system to recommend AirBnb in Bangkok to users using content-based filtering. 

### **Data**
Listing data was obtained from https://insideairbnb.com/get-the-data/ for the state of Bangkok, Thailand. 

### **Project Methodology**
1. Exploratory data analysis
- Analyzed distribution of key features such as listing price, number of accomodates, number of bedrooms and most common amenities.
- Imputed missing values using different techniques such as mode and mean imputation.
- Computed embeddings for listing description and neighbourhood overview using 'all-MiniLM-L6-v2'.

2. Clustering
- Performed K-Means and agglomerative clustering on above embeddings. Determined optimal number of clusters for K-Means clustering using elbow method. 
- Performed dimension reduction on embeddings using T-SNE to visualise goodness of seperation into clusters. Determined topics of description and neighbourhood overview for each cluster by looking at wordcloud and top 20 most common words in each cluster.

3. Recommendation system
- Users type in attributes such as number of guest, maximum price and must-have amenities. Users type in name of listing for system to return listings with similar description and neighbourhood overview.
- System filter listings based on inputted attributes. System filters listings to listings in similar cluster as the inputed listing name.
