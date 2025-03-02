Birds signal project

--------------------------------------------------DRIVE----------------------------------------------------
Google Drive folder link: 
	- https://drive.google.com/drive/folders/15a7PLBhTYxuN19gTcXYhckJCR-AAJsld?usp=sharing
	- #inside the Gdrive folder there are also the models and the handcrafted datasets used

--------------------------------------------------README----------------------------------------------------
The bird_signals_submission folder includes the following elements:

- Task1_audio_classification folder, which includes the notebook with all the code used to develop and evaluate the birdclef sound classification task. 
- Task2_image_classification folder, which includes the modeling and the evaluation notebooks with all the code used to develop and evaluate the birds species image classification task.
- Task3_image_retrieval folder which, includes the notebool with all the code used to develop and avaluate the birds species image retrieval.

- Birds_signals_presentation which are the slides for presenting the project

- crafted_data directory, which includes the handcrafted datasets for the evaluation (only in the drive)
- models_used directory, which contains the models used for audio and image classification (only in the drive)

- Demo notebook, which is the notebook to be used for performing the live demonstrations of the three tasks. The following key aspects of the demo notebook are worth mentioning:
    - The notebook can be devided in 3 macro sections: 
        - The datset and loading block, where all the dependencies an libraries are loaded and where the datasets needed are retrieved from Kaggle. 
        According this matter an API key is asked, that can be easily retrieved from the personal Kaggle profile. 
        During the demonstration we will locally load our personal API key which is not shared for privacy reasons.

        - The functions block, where all the function designed for the demo are grouped.

        - The tasks demos block, three sub blocks with all the code used to run the demo of each of the three tasks.

    - The demo exploits files stored on Google Drive, so is not possible to run the model locally unless the models are also loaded locally. 
     If the models are not retrievable automatically by the system a loading popup will come up, where will be possile to load the model.
     This allows also to make the demo usable for other future developed models.

- example folder, which includes some audio and images retrieved from the internet to perform the task in the demo notebook.
    - the images where collected from google images, by being sure that the species is included in the 525 classified.
    - the audio samples where collected from: https://xeno-canto.org, the file downloaded are in .mp3 format.
-------------------------------------------------Dataset_LINKS----------------------------------------------
Birdclef Bird sound classification:
    - https://www.kaggle.com/competitions/birdclef-2021/data
    - The audio labels are not directly the species name, this is how the dataset was built.
      to retrieve the actual species name you need to add after the slash of this link the label --> https://ebird.org/species/INSERT_LABEL
      This information can be helpful if you want to test the model with audio of birds coming from new sources. Or also to assess the actual species name.

BIRDS 525 SPECIES- IMAGE CLASSIFICATION:
    - https://www.kaggle.com/datasets/gpiosenka/100-bird-species