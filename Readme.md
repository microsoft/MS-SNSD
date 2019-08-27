# Microsoft Scalable Noisy Speech Dataset (MS-SNSD)
* This dataset contains a large collection of clean speech files and variety of environmental noise files in .wav format sampled at 16 kHz.
* The main application of this dataset is to train Deep Neural Network (DNN) models to suppress background noise. But it can be used for other audio and speech applications.  
* We provide the recipe to mix clean speech and noise at various signal to noise ratio (SNR) conditions to generate large noisy speech dataset. 
* The SNR conditions and the number of hours of data required can be configured depending on the application requirements.
* This dataset will continue to grow in size as we encourage researchers and practitioners to contribute to this dataset by adding more clean speech and noise clips. 
* This dataset will immensely help researchers and practitioners in accadamia and industry to develop better models. 
* We also provide test set that is different from training set to evaluate the developed models.
Further details of this dataset can be found in our Interspeech 2019 [paper](link to paper)

## Prerequisites
- Python 3.0 and above
- pysoundfile (pip install pysoundfile)
- ($ pip install -r requirements.txt)

## Please cite us if you use this dataset
[A scalable noisy speech dataset and online subjective test framework](link to the paper)

## MS-SNSD Dataset
# Training and test sets
1. Clean Speech data for training is present in the directory 'CleanSpeech'
2. Noise data for training is present in the directory 'Noise'
3. Noisy Speech for testing is present in the directory 'noisy_test'
4. Clean Speech corresponding to noisy speech test data is present in the directory 'clean_test'
Download the data onto your local machine.

## Usage
1. Clone the repo to your local directory
2. Download clean speech and noise datasets into the same directory with scripts
3. The repo contains the following files:
    - 'audiolib.py'
    - 'noisyspeech_synthesizer.cfg'
    - 'noisyspeech_synthesizer.py'
    - 'requirements.txt'
4. Specify your requirements in the config file (noisyspeech_synthesizer.cfg)
    - Specify sampling rate, audio format, audio length, silence length, total number of hours of noisy speech required and Speech to Noise Ratio (SNR) levels required.
    - Specify noise files to be excluded. Example: noise_types_excluded: Babble, Traffic. 'None' of no files to be excluded. 
    - Specify the path to noise and speech directories if it is not in the same directory as scripts. 
5. Noisy speech and the corresponding clean speech and noise files will be in the directories 'NoisySpeech_training', 'CleanSpeech_training' and 'Noise_training' respectively. 
6. Make sure that the config file is in the same directory as (noisyspeech_synthesizer.py) for ease of use.
7. Now run (python noisyspeech_synthesizer.py) to generate noisy speech clips.

