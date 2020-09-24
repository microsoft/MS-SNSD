# Microsoft Scalable Noisy Speech Dataset (MS-SNSD)
* This dataset contains a large collection of clean speech files and variety of environmental noise files in .wav format sampled at 16 kHz.
* The main application of this dataset is to train Deep Neural Network (DNN) models to suppress background noise. But it can be used for other audio and speech applications.  
* We provide the recipe to mix clean speech and noise at various signal to noise ratio (SNR) conditions to generate large noisy speech dataset. 
* The SNR conditions and the number of hours of data required can be configured depending on the application requirements.
* This dataset will continue to grow in size as we encourage researchers and practitioners to contribute to this dataset by adding more clean speech and noise clips. 
* This dataset will immensely help researchers and practitioners in accademia and industry to develop better models. 
* We also provide test set that is different from training set to evaluate the developed models.
* We provide html code for building two Human Intelligence Task (HIT) crowdsourcing applications to allow users to rate the noisy audio clips. We implemented an absolute category rating (ACR) application according to ITU-T P.800. In addition we implemented a subjective testing method according to ITU-T P.835 which allows to rate the speech signal, background noise, and the overall quality.
Further details of this dataset can be found in our Interspeech 2019 paper:
Chandan K. A. Reddy, Ebrahim Beyrami, Jamie Pool, Ross Cutler, Sriram Srinivasan, Johannes Gehrke. "A scalable noisy speech dataset and online subjective test framework," in Interspeech, 2019. [Link](https://www.isca-speech.org/archive/Interspeech_2019/pdfs/3087.pdf)

## Prerequisites
- Python 3.0 and above
- pysoundfile (pip install pysoundfile)
- ($ pip install -r requirements.txt)

## Please cite us if you use this dataset
```
@article{reddy2019scalable,
  title={A Scalable Noisy Speech Dataset and Online Subjective Test Framework},
  author={Reddy, Chandan KA and Beyrami, Ebrahim and Pool, Jamie and Cutler, Ross and Srinivasan, Sriram and Gehrke, Johannes},
  journal={Proc. Interspeech 2019},
  pages={1816--1820},
  year={2019}
}
```

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

## Dataset licenses
MICROSOFT PROVIDES THE DATASETS ON AN "AS IS" BASIS. MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, GUARANTEES OR CONDITIONS WITH RESPECT TO YOUR USE OF THE DATASETS. TO THE EXTENT PERMITTED UNDER YOUR LOCAL LAW, MICROSOFT DISCLAIMS ALL LIABILITY FOR ANY DAMAGES OR LOSSES, INLCUDING DIRECT, CONSEQUENTIAL, SPECIAL, INDIRECT, INCIDENTAL OR PUNITIVE, RESULTING FROM YOUR USE OF THE DATASETS.

The datasets are provided under the original terms that Microsoft received such datasets. See below for more information about each dataset.

The datasets used in this project are licensed as follows:
1. Clean speech: 
* PTDB-TUG: Pitch Tracking Database from Graz University of Technology https://www.spsc.tugraz.at/databases-and-tools/ptdb-tug-pitch-tracking-database-from-graz-university-of-technology.html; License: http://opendatacommons.org/licenses/odbl/1.0/ 
* Edinburgh 56 speaker dataset: https://datashare.is.ed.ac.uk/handle/10283/2791; License: https://datashare.is.ed.ac.uk/bitstream/handle/10283/2791/license_text?sequence=11&isAllowed=y 
2. Noise:
* Freesound: https://freesound.org/ Only files with CC0 licenses were selected; License: https://creativecommons.org/publicdomain/zero/1.0/
* Demand: https://zenodo.org/record/1227121#.XRKKxYhKiUk; License: https://creativecommons.org/licenses/by-sa/3.0/deed.en_CA

## Code license
MIT License

Copyright (c) Microsoft Corporation.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE
