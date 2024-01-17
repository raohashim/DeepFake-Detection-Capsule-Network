# DeepFake-Detection-Using-Capsule-Network
Please follow these steps to use the Capsule network in conjunction with VGG-19 to detect manipulation in faces:
1. Download the processed dataset from https://seafile.idmt.fraunhofer.de/u/d/b639276d15b9423bb11f/. Store the real images with "0_" as a prefix and fake images should have "1_", "2_", and "3_" as prefixes.

2. Extract frames from videos using the "Rename and Frame Extraction.ipynb" file and add only the directory path.

3. Follow the instructions in the "Data_Analysis.ipynb" file to create the test, train, and cv directory with cropped faces from the extracted frames.

4. Organize the database as described above before training the model. Change the parameters in the "train_binary_ffpp.py" file accordingly, such as the dataset path (where the train, test, and validation directories are located), checkpoints (where the model and its checkpoints will be saved), and dropout value. Check the source code for more details on parameters.

5. We trained three different capsule network variants using 5%, 10%, and 20% dropouts. The training files, checkpoints, and datasets are in their corresponding directories. Check the "CapsuleNet.ipynb" file for the evaluation results of the models.

6. Use the "test_binary_ffpp.py" file to evaluate the model on an unseen dataset or test dataset. Change the parameters, such as the saved checkpoint directory path and test data path.
