# 🖼️ YOLOv5 Object Detector 🚀

This project uses **[YOLOv5](https://github.com/ultralytics/yolov5)** for real-time object detection.  
You can run it on **images, videos, or even your webcam** to detect objects instantly.

# Why yolov5?
-YOLOv5 is used in this project because:
-It’s fast and lightweight → works in real-time with webcam.
-It’s accurate → can detect multiple objects in an image or video.
-It’s easy to train/customize → we can use pretrained weights (yolov5s.pt) or fine-tune on our own dataset.
-It supports different input sources → images, videos, and live camera feeds.

# 📂 Project Structure
.
├── detect.py          # Run detection
├── train.py           # Train YOLOv5 (if using custom data)
├── requirements.txt   # Dependencies
├── README.md          # Project guide
└── data/              # Images, videos, datasets


# 🛠 What to Install
-Python 3.8+
YOLOv5 works best with Python 3.8–3.10.

-PyTorch (torch & torchvision)
Core deep learning library. Without this, YOLOv5 won’t run.

-Example (CPU only):
pip install torch torchvision

# YOLOv5 dependencies
These are listed in requirements.txt, but the key ones are:
-opencv-python → to use webcam/video/images
-numpy → array/matrix handling
-matplotlib → drawing bounding boxes
-pandas, seaborn → for results visualization
-PyYAML → config file support
-Install all at once:
pip install -r requirements.txt

In short:
-Install Python
-Install PyTorch
-Install requirements.txt packages
-Download weights (.pt)

# How to run 
1. Open terminal (Anaconda Prompt recommended)
If you installed Anaconda, search "Anaconda Prompt" in your Start menu and open it.

2. Go to your YOLOv5 project folder
Example (if your project is in C:\Users\ashik\yolov5):
cd C:\Users\ashik\yolov5

3. Create a new Conda environment
conda create -n yolov5 python=3.8 -y

4. Activate the environment
conda activate yolov5

5. Install requirements
Inside the yolov5 folder, run:
pip install -r requirements.txt

6. Run with Webcam
-python detect.py --weights yolov5s.pt --source 0
-Opens your webcam.
-Press CTRL + C or close the video window to stop.

7. Run on a Single Image
python detect.py --weights yolov5s.pt --source data/images/sample.jpg

8. Run on a Folder of Images
python detect.py --weights yolov5s.pt --source data/images/

9. Run on a Video File
python detect.py --weights yolov5s.pt --source data/video.mp4

