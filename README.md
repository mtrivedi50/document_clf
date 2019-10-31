# Document classifier

The notebooks in this repository introduce a document classifier that's able to successfully distinguish between journal articles containing drug target information and those that do note.

If you're having trouble viewing the notebooks, please try viewing the notebook in Jupyter NBViewer: https://nbviewer.jupyter.org/

# Installation

**1. Create a project in the Google Cloud Platform**
  * Create an account with Google and navigate to the **Google Cloud console** web page: https://console.cloud.google.com/
  * Click **Select a Project** > **New Project**
  * In the **New Project** form, enter the name of the project, agree to the terms of service, and click **Create**

**2. Create and download a service account key**
* On the left-hand side of the **Google Cloud console**, click **IAM & admin** > **Service accounts**
* Click **Create Service Account** at the top of the screen
* In the details form, enter a name for the service account and click **Create**
* In the **Service account permissions** form, seleck **Project** > **Owner** and click **Continue**
* In the **Create key** form, click **Create key** > **JSON**, and then click **Create**

**3. Clone this repo onto your local machine and store the JSON file in the repo**

**4. Create a virtual environment and download the requirements (instructions below using Conda)**
* `cd document_clf`
* `conda create --name [NAME_OF_ENV] --file requirements.txt`

**5. Create a 'settings' folder in the directory where the environment stores its packages and details**
* `cd $CONDA_PREFIX`
* `mkdir settings`
* `cd settings`
* `touch __init__.py`
* Open the newly created `__init__.py` and create a variable `GOOGLE_CLOUD_CREDENTIALS` whose value is the string containing the name of the JSON downloaded during step 2

Note that the steps needed to create the Google Cloud Platform project and service key can be executed using the command line. More information on that here: https://cloud.google.com/sdk/
