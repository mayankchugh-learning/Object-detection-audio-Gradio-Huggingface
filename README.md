# Object-detection-audio-Gradio-Huggingface

### STEPS:
## How to run? 
### STEP 01- Create a conda environment after opening the repository
```bash
conda create -p objdetectionaudiovenv python -y
```

```bash
source activate ./objdetectionaudiovenv
```

### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```

### STEP 03- run application
```bash
python app.py
```

[Models -> Task -> Text-to-Speech -> License -> MIT -> kakao-enterprise/vits-ljs ](https://huggingface.co/kakao-enterprise/vits-ljs)

##### after download move the model to code folder
```bash 
sudo mv /Users/mayankchugh/.cache/huggingface/hub/models--facebook--detr-resnet-50 /Users/mayankchugh/gitRepos/mayankchugh.learning/Object-detection-Gradio-Huggingface/Model/models--facebook--detr-resnet-50
```
```bash
./Model/models--facebook--detr-resnet-50/snapshots/1d5f47bd3bdd2c4bbfa585418ffe6da5028b4c0b
```
##### after download move the model to code folder
```
cd /Users/mayankchugh/.cache/huggingface/hub/
```
### Prompt - draw_bounding_boxes
```bash
Write a python function code that will have 2 parameters, 1st one is the PIL image and second one is the object that contains the result. I have reveived from object detector model ([{'score': 0.7236634492874146, 'label': 'cat', 'box': {'xmin': 207, 'ymin': 229, 'xmax': 295, 'ymax': 344}}, {'score': 0.9842180013656616, 'label': 'cat', 'box': {'xmin': 208, 'ymin': 192, 'xmax': 296, 'ymax': 343}}, {'score': 0.99882572889328, 'label': 'dog', 'box': {'xmin': 314, 'ymin': 156, 'xmax': 462, 'ymax': 350}}]). the output should be the PIL image with all the objected highlighted with boundry.
```

### Prompt - generate_audio
```bash
Could you please write me a python code that will take list of detection object as an input and it will give the response that will include all the objects (labels) provided in the input. For example if the input is like this: [{'score': 0.9996405839920044, 'label': 'person', 'box': {'xmin': 435, 'ymin': 282, 'xmax': 636, 'ymax': 927}}, {'score': 0.9995879530906677, 'label': 'dog', 'box': {'xmin': 570, 'ymin': 694, 'xmax': 833, 'ymax': 946}}]
The output should be, This pictuture contains 1 person and 1 dog. If there are multiple objects, do not add 'and' between every objects but 'and' should be at the end only

```

[Gradio documentation link](https://www.gradio.app/docs/gradio/file)