# data-vizualisation
Using the Google Places API with a Database and
Visualizing Data on Google Map

In this project, we are using the Google geocoding API to clean up some user-entered geographic locations and then placing the data on a Google Map.

Google geocoding API is rate limited to fixed number of requests per day. So we might need to repeat the lookup process several times. So we break the task into two parts.

1. We read input file (where.data) one line at a time, and retrieve geocoded response and store it in a database (geodata.sqlite). Before we use the geocoding API, we check if we already have the data for that particular line of input in our DB.

2. Reads the database and writes tile file (where.js) with the location, latitude, and longitude in the form of executable JavaScript code.

Finally open where.html in a browser to see the locations. You can hover over each map pin to find the location that the gecoding API returned for the user-entered input.
