Installation
============

Requirements
------------

The project is implemented in Python and tested with:

* Python 3.10
* PyTorch >= 2.0
* NumPy, SciPy, scikit-image, OpenCV
* Pandas
* Gradio (for the web interface)

We recommend using a conda environment.

Setting up the Environment
--------------------------

Clone the repository and create the environment:

.. code-block:: bash

   git clone https://github.com/3220111903bit/BIA4_group_project_group8
   cd Droso

   conda create -n droso python=3.10
   conda activate droso
   pip install -r requirements.txt

Project Structure
-----------------

The core files and directories are organised as follows::

   Droso/
   ├── batch_inference_v2.py               # Batch inference (gene + sex)
   ├── gradio_app_gene_sex.py              # Gradio web interface
   │
   ├── feature_extraction/
   │     └── full_feature_extractor_v3.py  # Morphometric + venation features
   │
   ├── fusion_cnn_mlp_model/
   │     ├── fusion_best.pth               # Gene fusion model
   │     └── label2idx.json
   ├── fusion_cnn_mlp_sex_model_try_best/
   │     ├── fusion_best.pth               # Sex fusion model
   │     └── label2idx.json
   │
   ├── data/
   │     ├── reference_feature.csv
   │     └── crop_testing/                 # Example cropped wings
   │
   └── output/
         └── batch_inference_gene_sex.csv  # Example batch output

Once the environment is installed, the software can be used via the command-line
interface or the Gradio web interface, as described in :doc:`usage`.
