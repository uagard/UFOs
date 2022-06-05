# UFO

# Deliverable 2: UFO Sightings

## Overview of Project:

Dana created a webpage with an interactive table which shows data of multiple UFO sightings. She wanted to expand her search criteria options to provide a more in-depth analysis of UFO sightings. She wanted to allow the user to filter the data by utilizing multiple criteria at the same time. The filters included searching by date, city, state, country and shape.

## Results:

The app.js file starts out by importing the dataset from data.js. Through the process I went ahead and cleared out any existing data. Next I looped through each object in the data and appended a row and cells for each value in the row which was later filled by the values of each cell. 

The index.html file that was created from the classwork module already has the constructs of the webpage which would display the data. I was able to add the new syntax for the filter Search table which would take the user's inputs for dates, city, state, country and UFO shape. 

On the app.js, a variable was created to keep track of all the filters as an object. The function updateFilters() was used to update the filters. I saved the element, value and id of the filter that was changed as a variable. With the filter value was entered, I then added that filterID and value to the filters list. Otherwise the filter would be cleared from the filters object.

The function was afterwards called to apply all filters and rebuild the table. Function filterTable was used to filter the table when the data is entered. The filtered data was then set to tableData. Afterwards I used the following:

Object.entries(filters).forEach(([key, value]) = { 
filteredData=filteredData.filter(row=>row[key]===value);
});

this would allow me to loop through all of the filters and keep any data that matches the filter values. Finally, the table was rebuilt using the filtered data. Also, an event to listen for changes to each filter was also attached. Finally the table will be built when the page loads. 

Now that the JavaScript and HTML coding is complete, below is a snapshot of what the webpage looks like:

![Screenshot 2022-06-03 200220](https://user-images.githubusercontent.com/102105537/172069289-89cf2161-2c1a-4236-8b91-a0a1fc70e13b.png)

In order to conduct a search, the user only needs to the required info in the 'date', 'city', 'state', 'country' and/or 'shape' search boxes to filter the  UFO sightings data. Once the user has entered the desired criteria and press 'enter', the webpage will produce the filtered results after the 'click'. In order to refresh the page, the user can click the 'UFO Sightings' button located in the top left corner of the webpage.


## Summary:

WHile doing this project, drawback to the design. It is a possibility that the average user would not realize that the site has the capability to 'refresh' the table. The two items on this webpage I would recommend changing is to make it more user-friendly. First I would recommend the location of the 'UFO Sightings' button to below the criteria input boxes. Secondly I would recommend making the button stand out more in order to help the user navigate the site better.
