# Enhancing Scene Understanding for Vision-and-Language Navigation by Knowledge Awareness

## Setup Instructions

### 1.Requirements and Installation
  
1. **Install MatterPort3D Simulator:** Start by installing the MatterPort3D simulator from the official [repository](https://github.com/peteanderson80/Matterport3DSimulator).

2. **Install Python Dependencies:** Run the following command to install the necessary Python packages.
    ```setup
    conda create --name KESU python=3.8.0
    conda activate KESU
    pip install -r requirements.txt
    ```

3. **Download Dataset:** Download dataset from [Dropbox](https://www.dropbox.com/sh/u3lhng7t2gq36td/AABAIdFnJxhhCg2ItpAhMtUBa?dl=0), including processed annotations, features and pretrained models from [VLN-DUET](https://github.com/cshizhe/VLN-DUET). Put the data in `datasets` directory.

4. **Download Pretrained lxmert:**
   ```setup
   mkdir -p datasets/pretrained 
   wget https://nlp.cs.unc.edu/data/model_LXRT.pth -P datasets/pretrained
   ```
5.)**Download Pretrained Features and Trained-weights:**  Available [here](https://pan.baidu.com/s/1Q26O6j4lOxCOAmjWu0oHng?pwd=4kwf)
   
### 2.Pre-training  
To pre-train the model, execute the provided shell script.The following commands respectively start the pre-training for the R2R, REVERIE, and SOON tasks.
```pretrain
cd pretrain_src
bash run_r2r.sh
bash run_reverie.sh
bash run_soon.sh
```

### 3.Fine-tuning  
To fine-tune the model, execute the provided shell script.The following commands respectively start the fine-tune for the R2R, REVERIE, and SOON tasks.
```fine-tune
cd map_nav_src
bash scripts/run_r2r.sh
bash scripts/run_reverie.sh
bash scripts/run_soon.sh
```

### 4.Visualization
  
1. Trajectory visualization is provided by [Speaker-Follower](https://gist.github.com/ronghanghu/d250f3a997135c667b114674fc12edae)
