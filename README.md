# A simple web app using FastAPI and jinja2 templates

## Model training
Random Forest classifier has been used for training on the most popular Iris dataset. After training is complete, it will display model evaluation metrics and save the model in pickle format.

## Building the ML API using the FastAPI

1. Load the saved model from the irisModel.py file.
2. Create the Python class for inputs and prediction. Make sure you specify the data type. 
3. Then, create the predict function and use the `@app.post` decorator. The decorator defines a POST endpoint at the URL path `/predict`. The function will be executed when a client sends a POST request to this endpoint.
4. The predict function takes the values from the `IrisInput` class and returns them as the `IrisPrediction` class.
5. Run the app using the `uvicorn.run` function and provide it with the host IP and port number as shown below.

## Build a UI for the Web Application

Here instead of using the default swagger UI of FastAPI, Jinja2templates has been used which allows us to build a proper web interface using HTML files, enabling us to customize various components of the webpage.

1. Initiate Jinja2Templates by providing it the directory where HTML files will be. 
2. Define an asynchronous route that serves the "index.html" template as an HTML response for the root URL ("/").
3. Making changes to the input argument of the `predict` function using Request and Form. 
4. Defines an asynchronous POST endpoint "/predict" that accepts form data for iris flower measurements, uses a machine learning model to predict the iris species, and returns the prediction results rendered in "result.html" using TemplateResponse.

