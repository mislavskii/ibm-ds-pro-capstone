# Venuescape Explorer

Capstone project for IBM Data Science Pro Specialization on Coursera - in progress...

1. **Project Objectives:**

    - To explore existing business scenes in each of the city neighborhoods to find similarities and distinctions and, based on that data, build an automated system to identify prospective penetration routes. 
    The key objectives of such data science driven project can be summarized as follows: 

      + Generate exploratory description of city neighborhoods based on the business scene in each of them. Highlight similarities and distinctions by means of clustering; 
      +	Suggest preferable categories for opening a new venue in any given neighborhood; 
      +	Suggest preferable neighborhoods for opening a new venue of given category. 

2. **The Data. Acquisition, Processing, Analysis**

      To meet the above objectives, the following data will be required: 
     - The list of neighborhoods - that is, the low-level administrative divisions - in the city of choice. 
        + Can be obtained by web scraping using an algorithm in Python programming language from sources like Wikipedia or city administration website. 
          For example, if the target city were Bangkok, the capital of the Kingdom of Thailand, the lowest level administrative division would be subdistrict, or "khwaeng", 
          and there is a page titled "Khwaeng" on Wikipedia from which a list of all 180 neighborhoods across the city's 50 districts can be extracted 
        + In case the primary source doesn't include geographical coordinates, the list will have to be geocoded, for example, using the Geopy library for Python. 
     - The list of existing venues in each neighborhood. 
        + Can be acquired via API of a geoinformation system operator like Google or Foursquare. 
          For example, a "venues/search" endpoint request to Foursquare API returns a list of venues known to the service within a given radius around a geographical location point (latitude and longitude). 
          Obtained data will be persisted in an SQLite database according to a model developed on MySQL Workbench  and subject to K-Means clustering leveraging the capabilities of 
          Scikit-Learn package and Pandas dataframes with visualization in Folium maps / Matplotlib charts to discover similarities and distinctions between the city neighborhoods 
          in terms of the venue scene and generate recommendations as per the project objectives using an algorithm similar to those employed by existing media or goods recommender systems 
          envisaging locality itself as a prospective customer. 
3. **The Outcome**:
  - An automated venuescape penetration recommender in form of a Django-powered web application designed to suggest most-wanted categories per location or 
    best-prospect locations to open a venue in a given category. 

