# ROAD-ACCIDENTS-PREDICTION-AND-CLASSIFICATION
Final Year Project on Road Accident Prediction using user's Location,weather conditions by applying machine Learning concepts.

# DataSet
https://github.com/abdulwahed786/final-yr-projectqA

# To Run 
` python main.py `

# ML algorithms 
<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/29819481/67921930-4c64fe80-fbcf-11e9-9b87-c3225daad396.png">
</p>

# VM 
<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/29819481/67922038-8a622280-fbcf-11e9-828a-22fb0abd35b1.png">
</p>

Fig 4.6 Azure VM page

Virtual Machine deployed on Azure.

We have chosen Random Forest as our model as it has the highest accuracy (86.86%).

Input taken from user is sent to the backend flask server which feeds the parameters to the ML model and returns the result. It also sends a message to the police to take preventive measures.

**RESULTS AND DISCUSSIONS**


**Figure 4.1** User page

<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/29819481/67922275-56d3c800-fbd0-11e9-969c-ce6452b6d6a6.png">
</p>

The above figure 4.1 shows the home page of the web app. The web domain is secured with HTTPS wich has been obtained from the certificate authority for secure data transfer and to be able to use the Geolocation API. Displays the data owner login web page, which allows data owner to login and also to register, if the user does not have existing account.


**Figure 4.2** User Location by GPS

<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/29819481/67922304-681cd480-fbd0-11e9-8eb5-d8649e4d995c.png">
</p>

shows that when user clicks on update coordinates button, the web page requests the browser to take user coordinates. In the backend flask module, GeoLocation API is used to get location of the user. Ajax is used to update the latitude and longitude of the user in the web page.

The coordinates are sent to the OpenWeatherMap Api in the backend for the weather details. From the response we extract the details we require such as weather , road and light conditions.

Day of the week is updated with the getDate function of javascript.

**Figure 4.9** User input for other parameters

<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/29819481/67922808-e3cb5100-fbd1-11e9-9497-850fcf4061e0.png">
</p>

Figure 4.9shows the input for parameters taken from users. These include the vehicle type, age gender and speed limit.

**Figure 4.10** Output Predicted

<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/29819481/67922809-e463e780-fbd1-11e9-8eba-062a6662970c.png">
</p>

Figure 4.10shows all the data of the user. When the user clicks on Predict, that data is sent to the backend from where it is feeded into our chosen machine learning algorithm which is Random Forest. The output predicted is on the following basis of severity as 1- Fatal, 2- Severe, 3-Slight.

**Figure 4.11** Click on sms button

<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/29819481/67922806-e3cb5100-fbd1-11e9-884e-a89ef1bd4931.png">
</p>

In this Figure 4.11 an sms is sent to the police with location details and severity.  The TextLocal Api gives us 10 free messages to be sent every day.

**Figure 4.12** Map

<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/29819481/67922828-ecbc2280-fbd1-11e9-995b-1a9be5e3095c.png">
</p>

In the Figure 4.12 This web page displays an interactive heat map for users. Darker points mean greater severity. The gmaps api is used to plot on google maps.

<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/29819481/67922828-ecbc2280-fbd1-11e9-995b-1a9be5e3095c.png">
</p>
