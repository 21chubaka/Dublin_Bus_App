<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->



<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

# Dublin Bus App
Full Stack Software App Development Group Project
<!-- PROJECT LOGO -->

<br />
<div align="center">
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="https://github.com/21chubaka/Dublin_Bus_App/blob/main/dbus/src/assets/Dublin-Bus-logo.png" alt="Logo" width="320" height="160">
  </a>

<!-- <h3 align="center">Dublin Bus App</h3> -->
<!--
  <p align="center">
    Dublin Bus
    <br />
    <a href="https://github.com/othneildrew/Best-README-Template"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="http://ipa-011.ucd.ie/">View Live Project</a>
    ·
    <a href="https://github.com/21chubaka/dublinBus/issues">Report Bug</a>
    ·
    <a href="https://github.com/21chubaka/dublinBus/issues">Request Feature</a>
  </p>
-->
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#introduction">Introduction</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
        <li><a href="#run">Run</a></li>
      </ul>
    </li>
    <li><a href="#features">Features</a>
      <ul>
        <li><a href="#journey-planner">Journey Planner</a></li>
        <li><a href="#fare-calculation">Fare Calculation</a></li>
        <li><a href="#route-information">Route Information</a></li>
        <li><a href="#real-time-information">Real Time Information</a></li>
        <li><a href="#weather-information">Weather Information</a></li>
        <li><a href="#twitter">Twitter</a></li>
        <li><a href="#register-and-login">Register & Login</a></li>
        <li><a href="#dark-mode">Dark Mode</a></li>
        <li><a href="#mobile-optimization">Mobile Optimization</a></li>
      </ul>
    </li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



## Introduction
This project is a mobile optimised web application for Dublin's bus system.  The application
is designed to allow users to efficiently search for bus routes to their end destination.  In addition, 
the application provides accurate estimates of the travel time for a bus route to the user.  These
predictions are generated from Random Forest models built for the application.<br>
Below is a short demo of the application:

<div align="center">
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/README_imgs/Journey_Planner.gif" alt="Journey_Planner">
  </a>
</div>
  <h3>Make sure to click the marker icon after entering your address!<h3>

<p align="right">(<a href="#readme-top">back to top</a>)</p>



### Built With

* [![Vue][Vue.js]][Vue-url]
* [![Django][Django.com]][Django-url]
* [![Bootstrap][Bootstrap.com]][Bootstrap-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>



## Getting Started

This is an example of instructions on setting up your project locally.
To get a local copy up and running follow these simple example steps.

### Prerequisites

* npm
  ```sh
  npm install npm@latest -g
  ```

### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/21chubaka/dublinBus.git 
   ```
2. cd into the cloned directory
   ```sh
   cd dbus
   ```
3. Install NPM packages
   ```sh
   npm install
   ```
4. Install pip requirements & activate pipenv shell
   ```sh
   pipenv install --dev && pipenv shell
   ```

### Run
1. Serve the frontend
   ```sh
   npm run serve
   ```
2. Serve the backend. Note: You must be in pipenv shell at this point.
   ```sh
   python manage.py runserver 9000
   ```
3. Access App from frontend or backend
   ```sh
   http://localhost:8080/
   ```
   
<p align="right">(<a href="#readme-top">back to top</a>)</p>



## Features

### Journey Planner
Journey Planner allows the user to plan their trip by entering their starting and ending locations in the search box, 
or using their current location. Once locations are entered the user can click the Submit button and the route will
appear in the map, a fare calculation will appear in the lower right of their screen, and our model will return the 
predicted travel time above the map.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/README_imgs/Journey_Planner.png">
  </a>
</div>

### Fare Calculation
As mentioned above, users can view their fare by clicking on the Fare button. This is calculated by the
distance of the journey. All potential fare categories are displayed so the user does not have to
specify their age or whether they have a leapcard.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/README_imgs/fare_calculation.png">
  </a>
</div>

### Route Information
The route information feature allows users to search for the bus routes they want to view. Also, users can add their favorite routes to their favorites for future viewing and use.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/README_imgs/Route_Info.png">
  </a>
</div>

### Real Time Information
The user can select a bus stop on the map and view the expected arrivals of buses for that particular stop.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/README_imgs/RealtimeInfo.png">
  </a>
</div>

### Weather Information
he weather feature allows users to view the current weather in Dublin, tomorrow's weather and weather information for three days from now. This information includes temperature, feels like temperature and weather description information.<br>
<b>Current Weather</b>
<div>
    <a href="https://github.com/21chubaka/Dublin_Bus_App">
      <img src="/README_imgs/current_weather.png">
    </a>
</div>

<b>Tomorrow's Weather</b>
<div>
    <a href="https://github.com/21chubaka/Dublin_Bus_App">
      <img src="/README_imgs/tomorrow_weather.png">
    </a>
</div>

<b>Future Weather</b>
<div>
    <a href="https://github.com/21chubaka/Dublin_Bus_App">
      <img src="/README_imgs/future_weather.png">
    </a>
</div>

### Twitter
The Twitter feature allows users to view the latest tweets from Dublin Bus, so they can easily
view new information and alerts from Dublin Bus.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/README_imgs/Twitter.png">
  </a>
</div>

### Register and Login
The Register and Login features allow users to create their own account and display their username
on the page. Users’ information is stored in the database and verified with JWT-Authorization.
In addition, all functions are not affected if users do not login - there are no restrictions.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/README_imgs/Register.png">
    <img src="/README_imgs/Login.png">
    <img src="/README_imgs/login_completed.png">
  </a>
</div>

### Dark-Mode
The main purpose of dark mode is to facilitate use of the application at night. An added benefit
to the user is that dark mode has been found to have certain protective effects on people’s eyes
[5].

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/README_imgs/Dark_mode.png">
  </a>
</div>

### Mobile Optimization
The application is optimized for mobile, so users can use the application on their mobile
devices or personal computer. Every function in the navigation bar is placed in one button, and
can be viewed when users click on the button.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/README_imgs/mobile1.png" width="32%">
    <img src="/README_imgs/mobile2.png" width="32%">
    <img src="/README_imgs/mobile3.png" width="32%">
  </a>
</div>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Technical Approach

### Architecture & Tech Stack

### Front End

### Back End

### Communication between Front End & Back End

### Deployment

### Data Analysis & Data Management

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Testing & Evaluation

### Front End

### Back End

### User Testing

### Data Analysis

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING 
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
-->
<!-- <p align="right">(<a href="#readme-top">back to top</a>)</p> -->


<!-- LICENSE 
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p> 
-->



<!-- CONTACT -->
## Colleagues
[Gus Boothman](https://github.com/Gus1616)
<br/>
[Will O’Donohoe](https://github.com/21chubaka)
<br/>
[Cheng Zhang](https://github.com/20211342)
<br/>
[Xinhui Jiang](https://github.com/XinHuiUCD)

[Original Project Link](https://github.com/XinHuiUCD/dublinBus)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## References
[5] Henriette Eisfeld and Felix Kristallovich. The rise of dark mode: A qualitative study of an
emerging user interface design trend, 2020.




<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[Django.com]: https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white
[Django-url]: https://www.djangoproject.com

