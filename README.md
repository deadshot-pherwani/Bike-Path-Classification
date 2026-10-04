# Bicycle Lane Classification

This project uses smartphone sensor data to classify bicycle lane surfaces as smooth or bumpy.

## Setup

Use Python with Jupyter Notebook or VS Code with the Python and Jupyter extensions.

Install the required packages:

pip install numpy pandas scipy matplotlib scikit-learn minisom jupyter

Open the project folder, select your Python environment and run the notebook cells from top to bottom. Keep the data folder beside the notebook so the relative paths work.

## Dataset

Data were collected by three participants using the Sensor Logger app, recording the accelerometer, gyroscope and gravity sensors while cycling.

Each recording is stored in a separate folder inside `data`, containing:

- Accelerometer.csv
- Gyroscope.csv
- Gravity.csv

The files contain timestamps and measurements along the x, y and z axes. Recordings are labelled as smooth or bumpy in the notebook.

To add data, place the recording folder inside `data`, add it to the recordings dictionary and specify the trimming interval after inspecting the raw plots.

### Metadata

Each recording includes:

- Recording name: identifies the recording and its folder.
- Participant: identifies the person who collected it.
- Surface: smooth or bumpy.
- Trim interval: start and end times of the section used, in seconds.

After windowing, each window also has a recording name, window number, participant, surface label, start time and end time. These are stored in `window_metadata`, separately from the numerical features.

## Running the analysis

The notebook loads and trims the recordings, aligns the sensors, extracts window features and evaluates the models. Plots and explanations are included throughout.

After changing the data or settings, restart the kernel and run all cells again. Save the notebook with its outputs.

The independent deployment dataset is processed separately after choosing the final model.