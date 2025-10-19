# parking_lot_lehigh_hackathon

Inspiration: 
Oftentimes, when me and friends come back from a night drive, or soccer practice, or anything that requires us to use a car, we come back to this slight inconvenience of checking through every parking lot on campus that is close to where we live(maida). So we go around checking through trembly, front of m&m dorms, back of m&m dorms, dravo, and the other spots on campus. Of course we have our preference of trembly parking lot but oftentimes we are left with one available spot in the furthest parking in dravo. Lehigh has a slight issue with parking as they issued roughly the exact amount of permits as they have spots available so it can take a while to find a spot especially in the afternoon or late in the night. We developed this website to allow people to see availability in each parking lot so no time is wasted driving all across campus.

What it does: 
The website has each user sign up so it can create a unique id for each person. Once signed in, you get access to the map with the 5 parking lot locations(trembly, front of m&m dorm, back of m&m dorm, dravo road, dravo parking) that we used with colored dots symbolizing the availability of each parking lot.

How we built it: 
We utilized a series of AWS services but started off with amazon's location services and geofences to create the areas for the parking lots on campus. With this we got ids for the longitude and latitutde areas and we later used this in one of our lambda functions when requesting for user location to see if they are inside of the area of the parking lot. We did this to ensure that anyone trying to park or leave on the website was actually in the parking lot and not just reserving a spot before they are even there. We utilized dynamo db to store the locations and ran the thing on amplify to host the front end file for our website. We also utilized API gateway to give us a api or link for everything that we created to access it on your computer or phone.

Challenges we ran into: 
We had numerous challenges such as knowing how to integrate the various tools from AWS and have them work in tandem to create a working website as this is both our first time using AWS services. We also struggled with making sure that the geofence id was actually called and not just the latitude or longitude of the marker we put onto the map.

Accomplishments that we're proud of: 
We were very excited when we got the api to work and saw the working map and our first version of the website we were working on.

What we learned: 
We familiarized ourselves with some of the basic AWS services like amplify, dynamodb, and api gateway and feel more comfortable with the platform. We learned a bit of frontend because neither of us were very good or had experience with it.

What's next for lots: 
There were so many good ideas that we thought of a long the way that if we were to continue with the project we could make it a very deployable application for the university. Various logistics such as ensuring someone has pressed left when leaving a parking spot so that availability is not incorrect by notifying users if they are still in their spot every 8-12 hours, or having a rating system of how accurate they are with their parking status and how good they are with pressing park and leave appropriately.
