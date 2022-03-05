# SPEEMO-Speech-Emotion-Analyzer
Used RAVDESS dataset which included around 1500 audio files from 24 different actors to analyze emotions they represent Used dataset SAVEE which further had 500 audio files recorded by 4 different male actors Extracted the features from the audio files using LibROSA library in Python for audio analysis The model predicted the gender of the speaker with 100% accuracy It predicted the emotion of the speaker using 70% accuracy Accuracy can be improved by using more audio files for training
import sys
import pathlib

working_dir_path = pathlib.Path().absolute()

if sys.platform.startswith('win32'):
    TRAINING_FILES_PATH = str(working_dir_path) + '\\features\\'
    SAVE_DIR_PATH = str(working_dir_path) + '\\joblib_features\\'
    MODEL_DIR_PATH = str(working_dir_path) + '\\model\\'
    TESS_ORIGINAL_FOLDER_PATH = str(working_dir_path) + '\\TESS_Toronto_emotional_speech_set_data\\'
    EXAMPLES_PATH = str(working_dir_path) + '\\examples\\'
else:
    TRAINING_FILES_PATH = str(working_dir_path) + '/features/'
    SAVE_DIR_PATH = str(working_dir_path) + '/joblib_features/'
    MODEL_DIR_PATH = str(working_dir_path) + '/model/'
    TESS_ORIGINAL_FOLDER_PATH = str(working_dir_path) + '/TESS_Toronto_emotional_speech_set_data/'
    EXAMPLES_PATH = str(working_dir_path) + '/examples/'
