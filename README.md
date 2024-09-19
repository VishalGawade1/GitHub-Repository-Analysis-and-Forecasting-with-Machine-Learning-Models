
## Installation and Setup

### Prerequisites

- Python 3.8+
- Node.js 14+
- Docker
- Google Cloud account

### Backend (Flask)

1. Navigate to the Flask directory:
    ```bash
    cd src/Flask
    ```

2. Create a virtual environment and activate it:
    ```bash
    python -m venv venv
    source venv/bin/activate   # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

4. Run the Flask application:
    ```bash
    flask run
    ```

### Frontend (React)

1. Navigate to the React directory:
    ```bash
    cd src/React
    ```

2. Install the dependencies:
    ```bash
    npm install
    ```

3. Start the React application:
    ```bash
    npm start
    ```

### Forecasting Models

Each forecasting model has its own subdirectory under `src/Forecasting`. Follow the instructions in the respective `README.md` files to set up and run each model.

#### TensorFlow LSTM

1. Navigate to the Tensorflow_LSTM directory:
    ```bash
    cd src/Forecasting/Tensorflow_LSTM
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the model script:
    ```bash
    python model.py
    ```

#### Prophet

1. Navigate to the Prophet directory:
    ```bash
    cd src/Forecasting/Prophet
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the model script:
    ```bash
    python model.py
    ```

#### StatsModel

1. Navigate to the StatsModel directory:
    ```bash
    cd src/Forecasting/StatsModel
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the model script:
    ```bash
    python model.py
    ```

## Deployment

### Docker and Google Cloud

1. Build the Docker images for the Flask and React applications:
    ```bash
    docker build -t flask-app ./src/Flask
    docker build -t react-app ./src/React
    ```

2. Push the Docker images to Google Container Registry:
    ```bash
    docker tag flask-app gcr.io/your-project-id/flask-app
    docker tag react-app gcr.io/your-project-id/react-app
    docker push gcr.io/your-project-id/flask-app
    docker push gcr.io/your-project-id/react-app
    ```

3. Deploy the applications on Google Cloud using Kubernetes or Cloud Run. Follow the respective Google Cloud documentation for detailed steps.

## Design Diagram

![This diagram explains how the application workflow](https://github.com/shlokc9/Analyse-And-Forecast-GitHub-Repositories/blob/main/Design%20Diagram.png?raw=true)

## Final Report

The final report provides a comparative analysis of the forecasting models (TF/Keras/LSTM, Prophet, StatsModel). The recommendation for the best time-series forecasting model is based on the experimental results obtained.

## Contact

For any questions or feedback, please contact:
- Vishal Gawade: [vishalgawade311@gmail.com](mailto:vishalgawade311@gmail.com)
- Shlok Chaudhari: [shlokchaudhari9@gmail.com](mailto:shlokchaudhari9@gmail.com)
- Mihira Gudimetla: [gudimetlamihira@gmail.com](mailto:gudimetlamihira@gmail.com)
