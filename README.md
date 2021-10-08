# 3D-SPAD 

We referenced original 3D scene data from the SUNCG dataset. Please see the [webpage](http://suncg.cs.princeton.edu) and [paper](https://arxiv.org/pdf/1611.08974v1.pdf) for more details about the data.

### Content
3D-SPAD has 1500 3D scene samples. It includes three types of scenes: bedroom, bathroom, and living room. And there are 500 samples for each kind of scene. The 3D model data comes from the SUNCG dataset.

### Data Format
All 3D scenes are saved as "Dataset.json", and structured as follows:

Dataset.json
- scenes : array of scenes
    - scene_name : format(index+room type)
    - scene_assessment : The plausibility assessment of scene, 0=bad, 1=good
    - objects: array of objects in the scene
        - "id": The index of object in scene
        - "node_model_id" : corresponding model id for loading obj file in SUNCG dataset
        - "object_name" : corresponding model name for loading obj file 
        - "object_class" : corresponding model class for loading obj file 
        - "maxpoint": Bounding box maximum point
        - "minpoint": Bounding box minimum
        - "model_front": Initial orientation of the model
        - "rotation": The rotation of the object
        - "scale": Scale of model
        - "position": The position of the object
        - "object_assessment": The plausibility assessment of object, 0=bad, 1=good
