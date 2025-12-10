# IdaSky-Forcast
A repository to use in databricks to predict Idaho weather.

We want to build a model that makes predictions based off current temperatures for various Idaho weather stations. We will predict hourly, and weekly temperatures. Predictions will automatically create graphs and then we can even use leaflet to display real time graphs of Idaho wth shaded regions for color.

Perhaps we extend to the entire US?

Write your ideas below

Ideas:

Secret messagers

SQL database that holds the info we need for all weatherstations
Databricks jobs will grab the data automatically and keep the database up to date.
NiceGUI front/backend in docker containers hosted on the cloud. Will read from the database.
Second docker file on the cloud with a FastAPI backend. This backend will hold our pkl model so many apps can make predictions from the same model
Distributed system for Erlang?

Continuous training of model for upkeep
Store historical predictions for analytics?

Three Models:
1. Next Hours
2. Next Days
3. Given any lat/long, predict the weahter on a given day


Multiple front ends?
We can make multiple front ends, one for each state, and put them in their own docker. All front ends will use the same models so we can show how our model is scalable to end users. We can also learn kubernetes to seamlessly open all the docker files so it functions correctly

An erlang/ python server that has a queue and distributes the predictions to the correct models. We can stress test having 100000 people make predictions all at once to show how our system could distribute to various active models to ensure quick predictions.
