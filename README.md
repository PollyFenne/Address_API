# Address_API

## Task

We are building a neighbourhood collaboration site and we want to make a system to keep track of people, houses, and addresses of those houses.

Each person has a name, age and number of people in their household
Each house has an address and an owner
Each address has a postcode and street address
The REST API will need to enable users to:

Store people, houses and addresses
Look up a house, its address and owner
Look up people in our neighbourhood within certain age brackets and with specific household sizes

## Schema
![image](https://user-images.githubusercontent.com/113044818/204768700-444253f2-5194-4ac4-a57f-8da776fea92e.png)

## Handling Requests

### Storing people, houses and addresses: 
The API allows users to add a 'house' entry to the dataset using a POST method to the route '/houses'

### Look up a house, its address and owner: 
Users can pull a house's information by using GET methods to specific house IDs (i.e. /houses/2) or use the GET method to get all houses by using the path (/houses)

### Look up people in our neighbourhood within certain age brackets and with household sizes:
Users will input a minimum and maximum age and the API will present the people in the neighbourhood with an age in that range by using the GET method with a route that has a query parameter. The route would be (/houses/owner.age?min="inputMin"&max="inputMax"), this would return a JSON file with all houses that has a person within the age range.

## Routes
These are the routes that the API will need with their HTTP verb to enable users to perform lookups and create entries

POST /houses<br />
GET /houses<br />
GET /houses/:id<br />
GET /houses/owner.age?min=""&max=""<br />
GET /houses/owner<br />
GET /houses/address<br />

## Responses