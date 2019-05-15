# Mtcars_Flask_Api

A local flask API using the mtcars.csv dataset to create a predictive linear model with `mpg` as a reponse and (`disp`,`hp`,`drat`,`wt`,`qsec`) as predictors. This is using Python in a Docker container.

To run this API, open Terminal and change your directory to the docker folder. 

**Then run: `docker-compose up --build`**

**Open a new terminal under the same directory and run the curl command: `curl http://localhost:5000/`**   
You should get a response: `server is up - nice job!`
      
**To make a prediction of `mpg` using predictors, run the following command:
`curl -H "Content-Type: application/json" -X POST -d '{"disp":"160","hp":"100","drat":"3.9","wt":"3.15", "qsec":"17.6"}' "http://localhost:5000/predict_mpg"`**  
It will return as: `{"predict mpg": 21.182937457043106}`   
The predictor values can be changed and will result in different prediction returns.

**To stop your server running the API, type `ctrl-C`.** 
Check to see if you have any docker containers running using `docker container ls`, and stop them through `docker container kill <container-name>`.
