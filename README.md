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
        <li><a href="#register--login">Register & Login</a></li>
        <li><a href="#dark-mode">Dark Mode</a></li>
        <li><a href="#mobile-optimization">Mobile Optimization</a></li>
      </ul>
    </li>
    <li><a href="#technical-approach">Technical Approach</a>
      <ul>
        <li><a href="#architecture--tech-stack">Architecture & Tech Stack</a></li>
        <li><a href="#front-end">Front End</a></li>
        <li><a href="#back-end">Back End</a></li>
        <li><a href="#client--server-communication">Client & Server Communication</a></li>
        <li><a href="#deployment">Deployment</a></li>
        <li><a href="#data-analysis--data-management">Data Analysis & Data Management</a></li>
      </ul>
    </li>
    <li><a href="#testing--evaluation">Testing & Evaluation</a>
      <ul>
        <li><a href="#front-end">Front End</a></li>
        <li><a href="#back-end">Back End</a></li>
        <li><a href="#data-analysis">Data Analysis</a></li>
        <li><a href="#user-testing">User Testing</a></li>
      </ul>
    </li>
    <li><a href="#future-work">Future Work</a></li>
    <li><a href="#team-members">Team Members</a></li>
    <li><a href="#references">References</a></li>
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
    <img src="/media/Journey_Planner.gif" alt="Journey_Planner">
  </a>
</div>

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
    <img src="/media/Journey_Planner.png">
  </a>
</div>

### Fare Calculation
As mentioned above, users can view their fare by clicking on the Fare button. This is calculated by the
distance of the journey. All potential fare categories are displayed so the user does not have to
specify their age or whether they have a leapcard.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/fare_calculation.png">
  </a>
</div>

### Route Information
The route information feature allows users to search for the bus routes they want to view. Also, users can add their favorite routes to their favorites for future viewing and use.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/Route_Info.png">
  </a>
</div>

### Real Time Information
The user can select a bus stop on the map and view the expected arrivals of buses for that particular stop.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/RealtimeInfo.png">
  </a>
</div>

### Weather Information
he weather feature allows users to view the current weather in Dublin, tomorrow's weather and weather information for three days from now. This information includes temperature, feels like temperature and weather description information.<br>
<b>Current Weather</b>
<div>
    <a href="https://github.com/21chubaka/Dublin_Bus_App">
      <img src="/media/current_weather.png">
    </a>
</div>

<b>Tomorrow's Weather</b>
<div>
    <a href="https://github.com/21chubaka/Dublin_Bus_App">
      <img src="/media/tomorrow_weather.png">
    </a>
</div>

<b>Future Weather</b>
<div>
    <a href="https://github.com/21chubaka/Dublin_Bus_App">
      <img src="/media/future_weather.png">
    </a>
</div>

### Twitter
The Twitter feature allows users to view the latest tweets from Dublin Bus, so they can easily
view new information and alerts from Dublin Bus.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/Twitter.png">
  </a>
</div>

### Register & Login
The Register and Login features allow users to create their own account and display their username
on the page. Users’ information is stored in the database and verified with JWT-Authorization.
In addition, all functions are not affected if users do not login - there are no restrictions.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/Register.png">
    <img src="/media/Login.png">
    <img src="/media/login_completed.png">
  </a>
</div>

### Dark-Mode
The main purpose of dark mode is to facilitate use of the application at night. An added benefit
to the user is that dark mode has been found to have certain protective effects on people’s eyes
[5].

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/Dark_mode.png">
  </a>
</div>

### Mobile Optimization
The application is optimized for mobile, so users can use the application on their mobile
devices or personal computer. Every function in the navigation bar is placed in one button, and
can be viewed when users click on the button.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/mobile1.png" width="32%">
    <img src="/media/mobile2.png" width="32%">
    <img src="/media/mobile3.png" width="32%">
  </a>
</div>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Technical Approach
This section discusses the approaches used for the architecture of the system and the technical stack, 
the front end, the back end, client and server communication, deployment of the application, data 
analysis and management, and some justifications for these approaches.

### Architecture & Tech Stack
Vue JS acts as the front-end and Django acts as the back-end API. The stack is deployed within a
Docker container on the UCD server. A MySQL RDS database was utilised to store static data
like bus stop information and weather data, while the large amount of historical bus data is stored 
on UCD’s high performance server where the data analytics was carried out with Jupyter notebooks.<br> 
Below is an illustration of the architecture:

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/Architecture.png">
  </a>
</div>

### Front End
As a team, much deliberation was had over the technology to use for the front end. Vanilla
JavaScript, HTML, and CSS would have been very capable of satisfying the project’s specifications
and all team members were familiar with that technology. However, this project was seen as an opportunity 
to learn, and the decision to use a JavaScript framework was made. There are many benefits to frameworks, such as
easier asynchronous updates of the Document Object Model (DOM) and seamless page loading.
Drawbacks include that they can be overly complex for simple projects. Everything considered,
we decided to choose between React JS and Vue JS. There are pros and cons to both frameworks.
React is the most popular framework in industry. Vue uses HTML templates while React uses
JSX, this gives some familiarity to Vue due to our experience with HTML [11]. Performance wise
they are very similar. However, React is better suited to large scale web applications due to its
larger ecosystem. Ultimately, Vue was settled on due to it’s lightweight nature and lower barrier
to entry [11]. In particular, Vue version 3 was used, the latest version of Vue. Vue allowed for
the separation of the code into components like the Map or Navbar component. This meant the code was 
neater and less likely to cause code conflicts when merging. Another benefit to the framework is the 
access to libraries and plug-ins. For example, Vue3-google maps is a plugin that makes it easier to 
utilise the Google Maps API and the Vue date-time-picker, which is a ready made date and time selector plug-in. 
Furthermore, Vue3 can be packaged with the given vue-cli version and combined with the back end easily, 
which makes the development process relatively independent.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/vueComponets.PNG">
  </a>
</div>

### Back End
The decision on the technology for the back-end was more straightforward. From the start of
the project it was agreed to use Python for the back end services because of familiarity compared
to other programming languages. It was then debated which web framework to use between
Django and Flask. Both frameworks are very popular in industry. Django is better suited to more
complex projects due to it’s many ’out of the box’ features and libraries. For example, Django
has a ready made administration panel built-in, which scales better than Flask. Django enforces
best-practice software development due to it’s template structure [7]. Flask is less rigid and the
team already had experience with Flask. Ultimately, Django was chosen with the aim to
challenge ourselves and learn new technologies. The role of the back end includes connecting to
the database and acting as an intermediate between the front end and the database, combining
the front end and achieving the url redirect to the front end project and being deployed to the
server.

### Client & Server Communication
Passing data between the two frameworks (client and server), was acomplished by creating a
RESTful Framework API (Django) on the back end and using HTTP methods POST and GET requests to call 
these APIs on the front end. AJAX and the Fetch API were used on the front end to access the requests 
and response that were made on the back end. Some setting up was done to solve the Cross-Origin problem.

### Deployment
Since docker technology was used, this project was deployed on the container rather than directly
on the UCD VM Server. This container also opens the port 80 and 443 for HTTP and HTTPS
protocols. The SSH settings were set up on the container and the project source code was
uploaded to the container through Github. Then tmux was used to hang up the project so that it
could keep running even if logged out. In this way, the application is available to access through
the url (http://ipa-011.ucd.ie) <i>url now not active</i>.

### Data Analysis & Data Management
Historical bus data from 2018 which included information on vehicles, trips, and stop by stop data
was provided - most importantly planned and actual arrival times. In addition, historical weather
data from the Open Weather API was gathered, which matched the dates of the historical bus
data given. The weather data consisted of hourly measurements of various weather categories.<br>

A data quality plan was created and implemented. This included steps such as identifying rows
that were suppressed or had no arrival times and dropping them. Also before models were trained
the data was split (70/30) for training and test and shuffled.<br>

Various features to aid with data analysis and possible features to be used for the models were
created. Some included month as an integer from 1-12, day as an integer from 1-31, day of the
week as an integer from 0-6, weekend as a binary 0 or 1 (1 being Saturday or Sunday), and rush
hour as a binary (Excluding weekends: times between 8-9am and 4-6pm).<br>

After analyzing the weather and bus data the most correlated features were chosen. The final
features for the model were: month, day of the week, rush hour, hour, temperature, and wind
speed.<br>
- Month (month): int 1-12
- Day of week (dayOfWeek): int 0-6 Monday=0
- Rush hour (rushHour): int 0/1 8-9am and 4-6pm (Excludes weekends)
- Hour (hour): int 0-23
- Temperature (temp): float
- Wind Speed (wind speed): float<br>

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/correlation_matrix.png">
  </a>
</div>

Initially one route (39A) was chosen from the trip data to create models to predict the actual
duration difference (in seconds) from the planned duration time of a trip to the actual duration
time. In other words, if the trip took longer or shorter than planned. Three Linear Regression
models were created: one for the entire route 39A, one for 39A Inbound (Direction 1), and one
for 39A Outbound (Direction 2).<br>

Similar models were conducted for the leave time data-set, which is stop data as opposed to
complete trip data. For these models the arrival difference from stop to stop was predicted.
Along with Linear Regression, Decision Tree and Random Forest models were created from the
leave time data.<br>

These models and Linear Regression models from the trip data were rather poor and needed
improvement. None of these models had a cross-validated R2 score higher than 0.13 (Appendix
B: Fig B.1).<br>

The first step to improve the models was to combine the trip, leave time, and weather data-sets.
The data-set of historical bus (trip and leave time) and weather data when combined was about
117 million rows. The data was then split by route, first focusing on 39A.<br>

We again started with Linear Regression models for the entire route 39A. At this time, we included
Direction and Progress Number of the stop as features in these models. Progress Number (PROGRNUMBER) 
is the order of the stops the route takes from first to last. Again, these models did not perform 
any better (R2 = 0.13).<br>

We then moved to a Decision Tree model with a depth of 3 for the entire route 39A. As we
chose a depth of 3, we used Direction, Progress Number, and Month as our features. This model
performed basically identically to previous models.<br>

Finally, this approach was taken and used to create some Random Forest models. These models
did improve from previous iterations, but only marginally to an R2 of 0.23. Further improvement
was needed for the models.<br>

The data was split by route and by route directions. The route direction data sets varied greatly
in number of rows; the largest being over 2 million rows (Route 40 Direction 2) and the smallest
being almost 200 rows (Route 41D Direction 1).<br>

Random Forest models for the 39A Direction 1, and 39A Direction 2 were created. While noticeable 
improvement was observed, it was attributable to over-fitting caused by the use of the Progress Number 
feature.<br>

After excluding the Progress Number as a feature, the over-fitting issues were solved as the results
between training and testing were similar. Also, the best results for the models were observed,
thus far. The Cross-Validated R2 was 0.32 for Direction 1.<br>

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/model_progression.png">
  </a>
</div>

<table>
    <tr>
        <th>Name</th>
        <th>Type</th>
        <th>Features</th>
        <th>Metric</th>
        <th>Training Data</th>
        <th>Testing Data</th>
        <th>Cross-Validation</th>
    </tr>
    <tr>
        <td>All 39A</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
    </tr>
    <tr>
        <td>All 39A</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
    </tr>
    <tr>
        <td>All 39A</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
    </tr>
    <tr>
        <td>39A Direction 1</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
    </tr>
    <tr>
        <td>39A Direction 1</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
    </tr>
    <tr>
        <td>39A Direction 2</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
        <td>0</td>
    </tr>
</table>

After some further feature testing and testing our models with various estimators, we concluded
our models moving forward for the other routes would be a Random Forest model for each direction
of each route with an n-estimator of 20 and a random state of 42. It was important to keep our
estimators as low as possible without affecting the model’s performance, to support application
performance.<br>

As will be discussed in Testing & Evaluation, the 39A had some of our lower individual route-direction R2
scores. When applying this model approach to other route-directions, there was often improved
results.<br>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Testing & Evaluation
Below is an overview of the testing carried out for the front end, back end, and data analysis, as well as 
the user review surveys.

### Front End
Selenium web driver coupled with python’s unit test library was used to test the functionality and
logic of the application. Selenium is an automated testing library that is used to validate web
applications across different web browsers. Tests were written to assess the flow of the journey
planner. The logic of the sign up and log in were also tested. For example, it was tested that
if you already have an account the user could not sign up again. The appropriate responses to
these implementations were also tested.<br>

The chrome extension Google Lighthouse was also used to test the performance of the application.
Lighthouse runs a series of tests on a particular web page, and then generates a report on how
well the page performed. Failing tests were used as indicators on ways to improve the application.
The web page performed reasonably well on most metrics. Performance is where the greatest
improvement is needed. Lighthouse highlighted ways to improve this score, such as removing
unused JavaScript code, removing render blocking resources and setting defined dimensions for
images. SEO was our best metric which tested the page for features that are important to search
engines.

### Back End
To test the performance and scalability of the back end, some basic load testing using locust was
conducted. With 40 concurrent users making approximately 1 request per second, it was found
that most of the endpoints in the back end application had a mean and median response time of
less than 1 second after the implementation of suitable caching (see below). 

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/backend_req_resp_time.png">
  </a>
</div>

More users were then tested for scalability. The result was that no request failure was received 
even when there were 200 concurrent users (see below). It seems the performance of the back end 
is reasonably robust.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/request_test.png">
  </a>
</div>

### Data Analysis
Once the Random Forest models for each direction of each route were created, the evaluation
and validation scores of the models were compared. Below are the mean scores of all 252 models
created for the application.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/mean_model_scores.png">
  </a>
</div>

The average cross-validated R Squared across all models was 0.5638. This is essentially the
amount of variation that the models are able to account for using the features. Although higher
R Squared is the goal, this is higher than other published works [1]. The similar results across
training, test, and 3-fold cross-validation data sets does support a validated model without issues
such as over-fitting. The average Mean Absolute Error (MAE) of the models when predicting
actual bus arrival to a stop versus the planned arrival time is about 159 seconds, or 2.65 minutes.
This is also within the team’s original goals. MAE was used for evaluation over Mean Absolute
Percentage Error (MAPE) since the prediction is difference in arrival time, and zero as a prediction
is possible. In addition to the average performance across all models, the below graphs display
each model’s performance for R Squared, followed by MAE, when lining up the results from best
to worst. There is a line displayed for each direction. Interestingly, Direction 1 typically achieved
higher R Squared, but Direction 2 typically achieved lower MAE. Visibility into the range of model
results is useful to drive future work in addition to the average across all.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/cv_r2_scores.png">
  </a>
</div>

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/cv_r2_percentile_scores.png">
  </a>
</div>

The table above is individual route-direction results for those at the 75th, 50th and 25th percentiles
in R Squared performance. The inner quartile range for R Squared model performance is 0.46 to
0.74 for Direction 1, and 0.41 to 0.68 for Direction 2.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/cv_mae_scores.png">
  </a>
</div>

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/cv_mae_percentile_scores.png">
  </a>
</div>

The table above is individual route-direction results for those at the 75th, 50th and 25th percentiles
in MAE performance. The inner quartile range for MAE model performance is 120 to 210 seconds
(2 to 3.5 minutes) for Direction 1, and 113 to 182 seconds for Direction 2.

### User Testing
Incorporating the voice of the customer through user testing was very important for our application. 
User testing allowed the team to see what parts of the application worked or frustrated users, provided 
an unbiased view of the application, and avoided any ’tunnel vision’ by the developers. Each team member asked 2
to 3 people to review the application, answering the following questions:<br>

- Did you view the application on mobile or PC?
- How do you find aesthetics of the application? Is there anything you might change?
- How did you find using the features? How would you improve the features?
- Any additional comments?<br>

Eleven people reviewed the application. The overall response was largely positive with responses
highlighting the dark-mode, twitter page, and favourite features. As seen from the bar chart
below, the ratings are very high for overall aesthetics. It was noted that PC ratings were higher than
mobile, which most likely was due to the fact that the application was originally designed as a web application 
and then optimised for mobile.

<div>
  <a href="https://github.com/21chubaka/Dublin_Bus_App">
    <img src="/media/user_aesth_survey.png">
  </a>
</div>

While the surveys were completely anonymous, the responses were obtained from colleagues, friends and
family, so some bias may have impacted the results. However, constructive criticism was given. For
example, one user noted that the journey planning involved too many ’clicks’ in order to submit a
journey. The fact that the login option did not give any added functionality confused some users.
This was to be expected as the favourite routes were originally restricted, but became unnecessary
as this information was being stored in their local browsers.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Future Work

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
## Team Members
[Gus Boothman](https://github.com/Gus1616)<br>
[Cheng Zhang](https://github.com/20211342)<br>
[Xinhui Jiang](https://github.com/XinHuiUCD)<br>
[Will O’Donohoe](https://github.com/21chubaka)<br>

[Original Project Link](https://github.com/XinHuiUCD/dublinBus)<br>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## References
[1] Candis Anderson Enxi Cui Ankhit Pandurangi, Clare Byrne and Gavin McArdle. Design
and Development of an Application for Predicting Bus Travel Times using a Segmentation
Approach, 2020.<br>

[5] Henriette Eisfeld and Felix Kristallovich. The rise of dark mode: A qualitative study of an
emerging user interface design trend, 2020.<br>

[7] Devndra Ghimire. Comparative study on python web frameworks: Flask and django. 2020.<br>

[11] Maja Nowak. Vue vs react in 2022 - comparison of two most popular js frameworks.<br>

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[Django.com]: https://img.shields.io/badge/django-%23092E20.svg?style=for-the-badge&logo=django&logoColor=white
[Django-url]: https://www.djangoproject.com

