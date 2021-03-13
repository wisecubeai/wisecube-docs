# Nephos User Guide

### Overview
Nephos is a full-stack AI platform that allows data engineers and data scientists to manage datasets, explore them, create re-usable executables, build and run visual workflows that can train and publish models.

### Become a Beta User
Nephos is invite only currently. Contact info@wisecube.ai for a beta invite to the Nephos AI platform.

### Upload and Manage Datasets
Data is the lifeblook of any AI application. Nephos allows data scientists to upload datasets either as CSV files and also import data from S3 buckets and any open and accessible URI on the internet.

   - Click on the Datasets Tab
   - Click Create new Dataset
   - Upload a file from your local computer 
   - The system should import the new dataset  

### Explore Datasets 
Once the data has been imported as a dataset into the platform, you can then use your favorite Jupyter notebook environment to explore the dataset.
Here is how you can start exploring the dataset that you just imported:

   - Click on the Notebooks tab
   - A new Notebook session should launch
   - The datasets that are imported should be under ./nephos-core/resources/<resource-id>
   - You can find the resource-id of your dataset from the dataset list view.
   - You should be able to load it up into a [dask](http://www.dask.org) dataframe.


### Install Python Libraries
Even though we have pre-loaded tons of popular data science libraries into Nephos out of the box, There will be some times when we missed a few of your favorite ones. When you run into this situation there is an easy way to have them be installed into the Nephos environment.

   - Click on Libraries tab
   - Click on 'New Libaries' button
   - Select if you want to install a Single library or Multiple libraries at once.
   - Enter the library you would like installed or upload a requirements file.
   - Be sure to use the [pip requirements file format](https://pip.readthedocs.io/en/1.1/requirements.html#requirements-file-format) to specify your library and its version.

### Create Re-usable Executables
Once you have your notebook doing what you want to do, usually you want to package them into re-usable modules. In Nephos we call these executables. There are a few different ways you can create executables. Executables can either be binary files or also can be [papermill](https://papermill.readthedocs.io/en/latest/) based notebooks that take parameters. Either way all executables in Nephos need to take named input and output arguments specified.

   - Click on Executables tab
   - Click on 'New Executable' Button
   - If you are importing a [papermill](https://papermill.readthedocs.io/en/latest/) based notebook you can simply upload it by clicking the Code tab.
   - In this case Nephos should automatically parse the parameters and set them up as arugments to the executable.
   - You can give you executable a name and save them.
   - In case you are trying to use a binary file, you can upload it as well.
   - However you will have to register the input, output and string(flag) based arguments it takes.
  

### Build and Run Visual Workflows
Visual workflows are the heart of the Nephos platform. It brings together the data and the re-usable executables you have registered. 

   - Click on the Workflows tab
   - Open the Datasets/Executable side drawer by clicking on the Orange arrow on the right
   - You should be able to drag and drop datasets and executables you need onto the workflow canvas.
   - You can start building the worfklow by drawing arrows from datasets to executable input arguments.
   - You can also start connecting the output of one executable as the input to a different executable.
   - Nephos will automatically ensure the names of these match up even if they are called different things.
   - You can click on the 'Run' button to validate the workflow by quickly running it.
   - You can open the 'Run Info' drawer on the  bottom to see the output of the running workflow
   - Nephos will start preparing your workflow to run and show you progress and status of the runs


### Track all your related artifacts as a Project
A common problem in AI projects is that there is usually not a good way to track and manage datasets, notebooks, executables and workflows all in one central location. This is exactly why we have the concept of Projects in the Nephos platform. Here is how to create a Project and use it to track all relevant resources using it:

   - Navigate to the Projects tab and click on the 'New Project' buttonx
   - Give it in a name and use it to track other metadata about the project and its requirements as well.
   - Once you save the project, you can now start linking related resources to it.
   - Click on the 'Link Resource' icon on the Project row itself.
   - A dialog will open up that should allow you to select the kind of resource you want to link to it and search and link it to the Project.
   - Once you selected the right resource type and name, click on the 'Link' button to finalize linking it.



