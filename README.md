# Fire Weather Index (FWI) Predictor 
`https://fireweatherindex-predictor-production.up.railway.app`

This project is a web application built with Flask that predicts the Fire Weather Index (FWI) based on various environmental factors. It uses a Ridge Regression model trained on the Algerian Forest Fires Dataset.  

## Project Structure

- `app.py`: The main Flask application file.
- `Models/`: Contains the trained Ridge Regression model (`ridge.pkl`) and the StandardScaler (`scaler.pkl`) saved as pickle files.
- `templates/`: Contains the HTML templates for the web application.
  - `index.html`: The homepage with a welcome message and a link to the prediction form.
  - `home.html`: The prediction page with an input form for environmental factors and displays the predicted FWI.
- `requirements.txt`: Lists the Python packages required to run the application.
- `data/`: Contains the dataset used for training the model.
  - `Algerian_forest_fires_dataset_UPDATE.csv`: Original dataset.
  - `Algerian_forest_fires_cleaned_dataset.csv`: Cleaned version of the dataset used for model training.

## Setup and Installation

1.  **Clone the repository:**
   ```bash
   git clone <repository_url>
   cd FireWeatherIndex-Predictor
   ```

2.  **Create a virtual environment:**
   ```bash
   python3 -m venv venv
   ```

3.  **Activate the virtual environment:**
   - On Windows:
     ```bash
     venv\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv/bin/activate
     ```

4.  **Install the required packages:**
   ```bash
   pip install -r requirements.txt
   ```

## Running the Application

1.  **Ensure that the virtual environment is activated.**
2.  **Run the Flask application:**
   ```bash
   python app.py
   ```

3.  **Open your web browser and go to `http://127.0.0.1:5000/` to access the application.**

## Usage

1.  Navigate to the prediction page by clicking the "Get Started" button on the homepage or through the navigation bar.
2.  Fill in the input fields with the required environmental data: Temperature, RH (Relative Humidity), Ws (Wind Speed), Rain, FFMC (Fine Fuel Moisture Code), DMC (Duff Moisture Code), ISI (Initial Spread Index), Classes, and Region.
3.  Click the "Predict" button to get the FWI prediction.

## Model Information

The prediction is made using a Ridge Regression model, which is a type of linear regression that includes a regularization term to prevent overfitting. The model is trained on a preprocessed version of the Algerian Forest Fires Dataset. The data preprocessing steps and model training details can be found in the separate notebook (if available).

## Data Source

The dataset used in this project is the Algerian Forest Fires Dataset, which contains meteorological data and the corresponding FWI values. The dataset has been cleaned and preprocessed for use in model training.

## Future Improvements

- Input validation to ensure data quality. 
- More detailed error handling and user feedback.
- Expanding the range of models for comparison.
- Incorporating more features for improved accuracy.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

Thanks to the original data providers and the open-source community for the tools and libraries used in this project.
