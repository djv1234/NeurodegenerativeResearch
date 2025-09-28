# NeurodegenerativeResearch

This is the repository that I use to showcase some of the work I do in my role as an undergraduate researcher. Things like notebooks, files, and in the future my own model will be stored here. The first file I have added is my Colab notebook I used to organize the workflow for analyzing axon imaging from microscopy images. It combines dataset preparation, synthetic data generation for testing, and automated counting of intact vs. degenerated axons via using provided annotation files. 

Files used
- pics for Dmitry.zip - zip file provided to me with 4 .tif microscopy images, 4 corresponding XML annotation files, 4 labeled microscopy images. These files are used for training the model.
- Synthetic dataset under axon_dataset/train/images/, axon_dataset/train/labels/, axon_dataset/val/images/, axon_dataset/val/labels/

What the Notebook Does
File Handling
-Uploads and extracts .zip microscopy datasets.
-Lists and organizes .tif and .xml files for processing.
Environment Setup
-Installs required Python libraries (ultralytics, opencv-python-headless, pandas, torch, PyYAML).
-Configures GPU usage (Tesla T4 detected in Colab).
Synthetic Dataset Generation
-Creates artificial axon-like images (intact vs. degenerated).
-Annotates them automatically in YOLO format for potential model training.
Image Tiling
-Splits large (unedited) .tif microscopy files into smaller 1024×1024 .png tiles for easier analysis and training/quantification.
Annotation Parsing
-Parses CellCounter .xml files.
-Counts intact vs. degenerated axons.
-Outputs totals and ratio of degenerated to functional axons

