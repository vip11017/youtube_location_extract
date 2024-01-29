## Overview
Our goal is to develop a WebApp that, given a YouTube video URL, returns a map with a pin on each location mentioned. 
This will simplify your itinerary-planning: no more Googling places you heard from a video, our WebApp will do it automatically!
In addition, when you click on a pin, you'll see a link directing you to [booking.com](https://www.booking.com/index.it.html?aid=397594&label=gog235jc-1DCAEoggI46AdIM1gDaIkCiAEBmAEUuAEHyAEM2AED6AEBiAIBqAIDuAKHopWrBsACAdICJDZiZWNhNzcyLTVmZWYtNGUyYi1hMDMzLWQ0MTg4YjRmMmY2MtgCBOACAQ&sid=0091c803ef3b597482296dcd12748d99&keep_landing=1&sb_price_type=total&), where you can find hotels for that destination. 

## App walk through
1. Paste a YouTube video URL into the input box in the home page
2. When you hit search, the backend will generate a transcript of the YouTube video, analyze it using spaCy to find any Geopolitical Entities (GPEs) mentioned, and put them in a list
3. The list will be displayed on an interactive map using LeafletJS and Folium. Each pin will be a location mentioned in the video
4. When clicking on each pin, a box will appear. The link displayed on the box is a connection to the booking.com page for the specific location.
   
## Technologies
- spaCy (NLP tool)
- Geopy (Geolocation)
- LeafletJS/Folium (Interactive map)
- Flask (Webapp developemnt)
- Heroku (Webapp deployment)
  
## Challenges
. Disambiguation of location names: how does spaCy know if the 'Venice' mentioned in the video is in Italy or California?

. Optimization of WebApp and parallel processing: the tool is very slow as of right now; we are looking for a way to make it faster. 

. Misclassification of locations: sometimes, spaCy misclassifies people's names (or other instances) with locations.
