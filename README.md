# drivePro

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
drivePro will allow users to compare prices from various rental car enterprises and choose the best option.

### App Evaluation

- **Category: Productivity**
- **Mobile: Android**
- **Story: Tired of paying too much? Wanted a better rental car but couldn't afford it? View all of your options easily here!**
- **Market: Renters trying to be efficient and save money.**
- **Habit: Users can save deals to compare and get notified before the prices rise.**
- **Scope: Users will soon be able to book hotels/flights with great deals in accordance with their transportation.**

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

- [X] Creation of GitHub Organization and Group Project Repo (1pt)
- [X] App Overview: Description and evaluation (Mobile, Story, Market, Habit & Scope)
- [X] App spec: user stories, screens & navigation flows
- [X] Wireframe images 
- [X] Updated group info in the Course Portal: Group Name + App Description. 
- [X] User can login to drivePro application
- [ ] User can view vehicles available in the area
- [ ] User can view vehicle specs
- [ ] User can compare prices to similar vehicles


**Optional Nice-to-have Stories**

- [ ] Digital Wireframe/Mockup Images 
- [ ] Interactive Prototype gif

<!-- ### 2. Screen Archetypes

* [list first screen here]
   * [list associated required story here]
   * ...
* [list second screen here]
   * [list associated required story here]
   * ...
--> 



### GIF Walkthrough


<img src="gif21.gif" height="400" width="200">





### 2. Navigation

**Tab Navigation** (Tab to Screen)

* Home
* Reservations
* Search

**Flow Navigation** (Screen to Screen)

<image src="WireFrame 2.jpeg" width=600>

## Wireframes

<img src="wireframe.jpeg" width=600>


## Schema 
### Models
#### Registration

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | firstName     | String   | first name for vehicle registration |
   | lastName      | String   | last name for  |
   | Date of Birth | Date     | registrar's DOB to authenticate age validity |
   | Home Address  | String   | location of registrar in case of accident  |
   | Email         | Email    | primary mode of contact |
   | Phone         | Number     | secondary mode of contact |
   
#### Vehicle

   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | objectId      | String   | unique id for the specified vehicle |
   | Make          | String   | car manufacturer |
   | Model         | String   | model of car  |
   | Year          | Number   | year the car was manufactured |
   | Price Per Day | Number   | cost to rent the vehicle per day |
   | Our Rating    | Number   | how does this vehicle's quality and price per day compare to others like it |
   | Similar Vehicles  | Image | vehicles of similar size (compact, mid-size, full-size) |
   
#### Rental Agency
  
   | Property      | Type     | Description |
   | ------------- | -------- | ------------|
   | Company       | String   | name of rental agency |
   | Location      | String   | physical address to pick up the car |
   | Age Requirement  | String   | how old you have to be to rent from this agency  |
   | Fees          | Number   | payments in addition to price per day |
   | Company Phone Number | Number   | primary mode of contact |
   | Company Email    | Email  | secondary mode of contact |
  
  
  #### API's  
  
  | Rental | Reservation |  Model | Year | Car
| ------------- | ------------- | ---------| --------| -------|
| Car Rental    | Reservation   | Model    | Year    | Car    |
| Car Rental    | geo_search    | Location |         |        |
  
   

   
   
#### Networking
- [Add list of network requests by screen ]
  
 ####Network Request
  
  | Rental | Http |  Example
| ------------- | ------------- | ---------| 
| Create  | Post   | Create User      |
| Update  | Get    | Rentals          |  
| Read    | Get    | User Information |
  
  
  
  ```
  
  Home Feed Screen
(Read/GET) Read in Username and Password
(Create/POST) Create List of Rentals
(Create/POST) Create Categories of Rentals.
(Delete) Delete existing comment
Create Post Screen
(Create/POST) Create a new post object
Profile Screen
(Read/GET) Query logged in user object
(Update/PUT) Update user profile image
  
  ```
  
- [Create basic snippets for each Parse network request]
  
  ```
  
  ##Parse Query Code Snippet
  '''Java
  it('should get PII via API with Get using master key', done => {
   Parse.User.logOut().then(() =>
    new Parse.Query(Parse.User)
     .get(user.id, { useMasterKey: true })
     .then(fetchedUser => {
      expect(fetchedUser.get('email')).toBe(EMAIL);
      expect(fetchedUser.get('zip')).toBe(ZIP);
      expect(fetchedUser.get('ssn')).toBe(SSN);
      done();
     })
   );
  });
  
  ```
  
- [OPTIONAL: List endpoints if using existing API such as Yelp]

  ```
  
  #API's Links
  https://www.etravos.com/car-rental-api-integration.html
  
  https://developer.sabre.com/docs/rest_apis/utility/geo_search
  
  https://www.travelopro.com/car-rental-reservation-system.php  
 
```
  
  
  ##Sprint planned for next week 
  
  The plan for next week is to have a completely designed login_xml, signup_xml and have both screens fully functional. The issues created are the implementation of specific design features and functions are more challenging than previously thought. Different parts of the project will be sent to individuals in the group. On the login_xml I added a LinearLayout inside of a LinearLayout with google functions. Which I and the group plan to have to work definitely by the next unit. 
  
  
   
   
  
  ##Updated status of issues in Project board
  
  An issue with the SSL Projects error occurred. Causing the program not to compile correctly. This issue was resolved by going into setting's/System Settings/Android SDK/ SDK Update sites. The sites were checked and updated. Causing the program to work properly.

Animations are added to the start home screen of the program. Multiple XML files are created for
different functions of the app. 
  
  An issue of the app not reading in the google API's occured when the program was not runnin in Administartor mode for Android Studios
  
  During this phase trying to add more more layout features and buttons to the activity_login.xml, the issues arrived of the OnCliclListener causing the program to crash so I had to go back and look at it. Changing some code around.
  
