# Requirements #
#### Built models on tensorflow 1.12
#### Download models from google drive here - https://drive.google.com/open?id=1GL4RvYcOSBJOKU9H7sjmNI-3XNSYe9Mj - and add this folder to the 'inputs' folder. Will take around 20 mins to download

# Usage 
### Make sure you have the folder structure as it is in the github repo and you download the models from the above link 
python pcb_errors.py --input_image=1.1.jpg

# Accuracy
My main focus was on True Negatives(~>90%), since the problem statement was to find errors in any pcb, having a high TN is necessary so that we do not miss any defective pcb. The disadvantage of focusing on TN was that the False Negatives also started increasing. If there was more time, it should have been possible to decrease FN.

# Approach
Observing all the images under labelImg app gave the idea that all the components places are fixed with very little variations. Additionally, have build the models only for missing parts which are missing in the data provided. Similarly, for rotated parts as well. For eg: compononent 1_a is present through out the data correctly, hence have not built missing or rotated models for this components.
Then broke the problem down in three parts:
1. Missing + Rotation
2. Only Missing
3. Only Rotation
