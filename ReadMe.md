Check if the browser supports geolocation.

Set options for high accuracy, a 5-second timeout, and no caching.

Use watchPosition to track the user's location continuously.

Emit the latitude and longitude via a socket with "send-location". 

Log any error to the console. 

Initialize a map centered at coordinate (0,0) with a zoom level of 16 using leaflet. 

Add open stream map tiles to the map. 

Create an empty object marker. 

When receiving location data via the socket, extract ID, latitude, and longitude and center the map on the new coordinate. 

If a marker from the ID exists, update its position, otherwise, create a new marker at the given coordinate and add it to the map. 

When a user disconnects comma, remove their marker from the map and delete it from markers.