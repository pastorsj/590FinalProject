# ANLY 590 Final Project

This project seeks to count the number of two different types of Bollworms (ABW and PBW) in images. This is done in response to a [Zindi competition](https://zindi.africa/competitions/wadhwani-ai-bollworm-counting-challenge).

Three different models are built to solve this problem: YOLO, Faster R-CNN, and Mask R-CNN. The repository contents are shown here as a map to the project model building.

Repository Contents:
- `data/`
    - contains data needed for the analysis (testing data, training data, bounding box information)
    - the actual images are not committed here for storage but can be found on the [competition website](https://zindi.africa/competitions/wadhwani-ai-bollworm-counting-challenge)
- `models/`
    - YOLO code
        - `dataset.yaml`
        - `yolov5s.pt`
        - `yolo-data-preparation.ipynb`
        - Note:
            - Run with: `python train.py --img 640 --batch 16 --epochs 5 --data dataset.yaml --weights yolov5s.pt`
            - Trained utilizing a pre-trained model from an [external repository](https://github.com/ultralytics/yolov5) which is not committed here.
    - Faster R-CNN code
        - `rcnn-data-preparation.ipynb`
        - `rcnn.ipynb`
        - Note: 
            - PyTorch-based model
    - Mask R-CNN code
        - `detectron2-data-preparation.ipynb`
        - `detectron2_mask_rcnn.ipynb`
        - Note:
            - PyTorch-based model
    - `data-sourcing.ipynb`
        - used to get all of the images from the competition website onto local computer
- `project_documents/`
    - contains the original project proposal and the final project summary
- `results/`
    - contains results from all of the models for use in visualizing and understanding model results