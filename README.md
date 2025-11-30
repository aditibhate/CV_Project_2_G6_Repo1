STEPS TO GET DATASET FROM ROBOFLOW 

DATASET USED FOR THIS PROJECT : https://universe.roboflow.com/myroboflow/multitrash

Step 1: Run the Notebook as it is (preferably on cloud for faster training)

Step 2: Open an account on ROBOFLOW to get the Dataset

-Once you're logged in:

-Click on the project that contains the dataset you want.

-You will see the dataset page with images and annotation info.

Step 3: Click “Download Dataset”

-On the left-hand side, find and click:

-Download Dataset

-Sometimes it's at the top right depending on your layout.

Step 4: Choose a Format

-A list of export formats will appear (example: YOLOv8, COCO JSON, Pascal VOC, etc.).

-Choose the one your code needs.

-Example: choose YOLOv8 if you are using Ultralytics.

Step 5: Get the Download Code

-After choosing the format, scroll down to the section titled:

-"Download with Roboflow API"

OR

-"Install & Use in Python"

You will see code like this:

from roboflow import Roboflow

rf = Roboflow(api_key="YOUR_API_KEY")

project = rf.workspace("your-workspace").project("your-project")

dataset = project.version(1).download("yolov8")

##MIGHT LOOK DIFFERENT ACCORDING TO YOUR PROJECT DATASET

Step 6: Copy the Code

-Copy the code snippet into your Python script or Jupyter notebook.

-Replace:

"YOUR_API_KEY" with the API key shown on your page

"your-workspace" with the workspace name

"your-project" with the project name

version(1) with the correct version number

Step 7: Run the Script

-Run your Python script.

-Roboflow will AUTOMATICALLY:

- authenticate with your API key

- download the dataset

- unzip it

- create a folder like:

your-project-1/

    ├── train/
    
    ├── valid/
    
    ├── test/

#ALL THESE STEPS WILL HAPPEN AUTOMATICALLY
