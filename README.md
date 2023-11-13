# AI-Powered CT Segmentation & Segmentation Automation

The goal of this project is to generate segmentation masks for full-body CT scans through MONAI and PyTorch and automate the generation process using Python scripts in a DICOM SCP.

Project features:

-   AI-generated whole-body CT Segmentation mask.
-   Organ volume computation.
-   Automation of the segmentation process using Python and a DICOM SCP server.

Access the CT Segmentation notebook from [here](/src/notebooks/segmentation-model.ipynb).

### Progress so far

-   Render coronal slice of the raw image using pyplot.
-   Jupyter notebook to run the segmentation model on a CT WB from NBIA as a POC.
-   Organ volume computation through `voxel count` and `channel_def` metadata.

### TODO

-   Automation and routing scripts using pydicom and orthanc server.
-   Migrate model codebase from notebook to the main python script.
-   Dockerfile to containerize the model and osimis/orthanc base image.
-   GitHub workflow pipeline for building the docker image.

### Automation diagram

![](https://app.eraser.io/workspace/cjrCbf2cbEThTzrVtSey/preview?elements=ayP71t1lAoQTPv-CEpXxsQ&type=embed)

### Project specs

-   Python v3.11.x [packages](/requirements.txt)
-   Docker compose
    -   osimis/orthanc
    -   postgres:14
-   MONAI
    -   Whole Body CT Segmentation Model
