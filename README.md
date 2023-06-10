# Flask App for Yandex.Realty Apartment Price Prediction

This project is a Flask application that utilizes a machine learning model to predict the price for renting apartments on Yandex.Realty. The application takes four input parameters and provides an estimated rental price based on these inputs.

## Source Data and Model Statistics

The machine learning model used in this project was built using the following source data:

- Dataset: Yandex.Realty apartments data
- Features: 4 input parameters (open_plan, rooms, living_area, renovation)
- Target variable: Rental price

To clean and preprocess the data, the following steps were performed:

1. Data cleaning: Removing missing values, handling outliers, and resolving inconsistencies.
2. Feature engineering: Extracting relevant features from the data and transforming them as needed.
3. Feature scaling: Applying scaling techniques to ensure all features are on a similar scale.


## Installation and Running the App

To install and run the Flask application locally, please follow these instructions:

1. Clone the repository:

   ```bash
   git clone <repository-url>
   cd <repository-name>
   ```

2. Set up a virtual environment (optional but recommended):

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Run the Flask application:

   ```bash
   python app.py
   ```

   The application will be accessible at `http://localhost:5444` in your web browser.

## Dockerfile

The project includes a Dockerfile to facilitate containerization of the application. The Dockerfile contains the necessary instructions to build a Docker image for the Flask application.

```

The Dockerfile specifies a base image with Python 3.8, sets the working directory to `/app`, copies the project files into the container, installs the dependencies from `requirements.txt`, exposes port 5000 for the Flask application, and sets the command to run `app.py`.

## Opening the Port on a Remote VM

To open the port on a remote VM, follow these general steps:

1. Access your remote VM using SSH or any other remote access method.
2. Configure the firewall settings to allow incoming connections on port 5444.
3. If using a cloud service provider, check their specific documentation on how to configure network settings and open ports.

## Running the App Using Docker

To run the Flask application using Docker, follow these steps:

1. Pull the Docker image from Docker Hub:

   ```bash
   docker pull asvad/e2e23_price_predictor:v.0.1
   ```

2. Create and run a Docker container:

   ```bash
   docker run --network host -it asvad/e2e23_price_predictor:v.0.1
   ```

   The `--network host` flag allows the container to access the host's network, which is required to access the Flask application running inside the container.

3. The Flask application inside the Docker container will be accessible at `http://localhost:5444` in your web browser.
