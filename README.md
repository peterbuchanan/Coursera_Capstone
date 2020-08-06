# IBM Applied Data Science Report

## Evaluate metropolitan Adelaide hotel locations by net gaming revenue, population density and traffic volume

[Peter Buchanan](https://www.linkedin.com/in/buchananpeter/) - April 2020

<img src="images/shutterstock_262869080-1.jpg" width="60%" align="center"/>

### Table of Contents
* [4. Data Preparation](#4.-Data-Preparation)
    * [4.1. Download and Unzip Files](#4.1.-Download-and-Unzip-Files)
    * [4.2. Read files into Dataframes](#4.2.-Read-files-into-Dataframes)
    * [4.3. Hotel Dataset: Clean](#4.3.-Hotel-Dataset:-Clean)
    * [4.4. Hotel Dataset: Update GoogleAPI Geocoding](#4.4.-Hotel-Dataset:-Update-GoogleAPI-Geocoding)
    * [4.5. Hotel Dataset: Merge Australian Bureau of Statistics (ABS) and Australian Tax Office (ATO)](#4.5.-Hotel-Dataset:-Merge-Australian-Bureau-of-Statistics-(ABS)-and-Australian-Tax-Office-(ATO))
    * [4.6. Gaming Revenue Dataset: Clean](#4.6.-Gaming-Revenue-Dataset:-Clean)
    * [4.7. Top Net Gaming Revenue Cities Dataset: Clean](#4.7.-Top-Net-Gaming-Revenue-Cities-Dataset:-Clean)
    * [4.8. Hotels in Top Net Gaming Revenue Cities Dataset](#4.8.-Hotels-in-Top-Net-Gaming-Revenue-Cities-Dataset)    
    * [4.9. Shopping Malls Within Top Net Gaming Revenue Cities Dataset: Clean](#4.9.-Shopping-Malls-Within-Top-Net-Gaming-Revenue-Cities-Dataset:-Clean)
    * [4.10. BeautifulSoup: Top Net Gaming Revenue LGA Cities Census Dataset: Clean](#4.10.-BeautifulSoup:-Top-Net-Gaming-Revenue-LGA-Cities-Census-Dataset:-Clean)
    * [4.11. FourSquare Dataset: Venue Categories Clean](#4.11.-FourSquare-Dataset:-Venue-Categories-Clean)
    * [4.12. FourSquare Dataset: Venue Explore: All Categories for Top NGR Cities ( HierarchyLevel 1 to 5 )](#4.12.-FourSquare-Dataset:-Venue-Explore:-All-Categories-for-Top-NGR-Cities-(-HierarchyLevel-1-to-5-))
    * [4.13. Pickle Pandas Dataframes](#4.13.-Pickle-Pandas-Dataframes)    
* [5. Analysis and Machine Learning](#5.-Analysis-and-Machine-Learning)
    * [5.1 Exploratory Data Analysis (EDA)](#5.1-Exploratory-Data-Analysis-(EDA))
    * [5.2 Choropleth: Ranking of Local Government Area/Group by Average NGR per machine](#5.2-Choropleth:-Ranking-of-Local-Government-Area/Group-by-Average-NGR-per-machine)
    * [5.3 Barchart: Average Net Gaming Revenue per machine (2018/19) by Local Government Area](#5.3-Barchart:-Average-Net-Gaming-Revenue-per-machine-(2018/19)-by-Local-Government-Area)
    * [5.4 Barchart: Average Net Gaming Revenue per venue (2018/19) by Local Government Area](#5.4-Barchart:-Average-Net-Gaming-Revenue-per-venue-(2018/19)-by-Local-Government-Area)
    * [5.5 Barchart: Population by City in Local Government Area (Campbelltown / Tea Tree Gully)](#5.5-Barchart:-Population-by-City-in-Local-Government-Area-(Campbelltown-/-Tea-Tree-Gully))
    * [5.6 Choropleth: City, Hotel, Shopping Mall, Foursquare search radius and Traffic Volume](#5.5-Choropleth:-City,-Hotel,-Shopping-Mall,-Foursquare-search-radius-and-Traffic-Volume)
    * [5.7 K-Means Cluster Analysis Of Cities by Foursquare Category](#5.6-K-Means-Cluster-Analysis-Of-Cities-by-Foursquare-Category)
    * [5.8 KElbowVisualizer: The Optimal K-Cluster with Elbow Method](#5.7-KElbowVisualizer:-The-Optimal-K-Cluster-with-Elbow-Method)
    * [5.9 Top Ten Most Common Venues by City](#5.8-Top-Ten-Most-Common-Venues-by-City)
    * [5.10 Choropleth: Visualize Clusters by City](#5.9-Choropleth:-Visualize-Clusters-by-City)
    * [5.11 Examining distributional characteristics of clusters](#5.10-Examining-distributional-characteristics-of-clusters)    
    * [5.12 Cluster 0: Quiet Suburban](#5.11-Cluster-0:-Quiet-Suburban)
    * [5.13 Cluster 1: Rural](#5.12-Cluster-1:-Rural)
    * [5.14 Cluster 2: Recreation Park](#5.13-Cluster-2:-Recreation-Park)
    * [5.15 Cluster 3: Busy Area (Shopping Malls, Densely Populated, High Traffic Volume)](#5.14-Cluster-3:-Busy-Area-(Shopping-Malls,-Densely-Populated,-High-Traffic-Volume))
    * [5.16 Cluster 4: Recreational Area (Golfcourse, Gyms, Parks)](#5.15-Cluster-4:-Recreational-Area-(Golfcourse,-Gyms,-Parks))
