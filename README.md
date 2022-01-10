# Sharing Projects with DVC-tracked data files
This repo is to demonstrate a dvc pipeline when the data is stored outside the git repo. 

# Publicly Shared Google Drive Folder
The data for this DVC pipeline is in a public GDrive folder which you can access using this link:

https://drive.google.com/drive/folders/1akKKb2qHrMLq1cBYgCQ_9Orx9Q9Wzpfe?usp=sharing

# How-To

```{bash, eval = FALSE}
# Clone the project repo 
# Using SSH
git clone git@github.com:GavinMasterson/dvc-share-demo.git

# OR using HTTPS
git clone https://github.com/GavinMasterson/dvc-share-demo.git

# Go to folder
cd dvc-share-demo

# Get the data based on the info in the .dvc/config file 
dvc pull
```
Follow the link that is shown to you and give DVC full permissions to access and edit the drive folder.  
Some error messages will be thrown because some files are missing from the pipeline contained in `dvc.yaml`.  
Don't worry - these files are created by the pipeline

```{bash}
# Run the pipeline
dvc repro
```

The pipeline will now run produce the final output: `report.html`.
