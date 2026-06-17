This is the official repository for the paper **MEC: Medical Evidence Capsules for Retrieval-Augmented Generation in Medical Multimodal Question Answering**.

## Data Resources

This repository contains only a small number of example samples for quick reference to the data structure and format. Due to the large size of the dataset, the full data resources are hosted on ModelScope.  Please access them at:

> 🔗 [https://www.modelscope.cn/datasets/morefree6/MEC](https://www.modelscope.cn/datasets/morefree6/MEC)



## Usage Notice

- The MEC dataset is constructed from multiple underlying data sources, each governed by its own license agreement. **Please refer to the ModelScope page above for detailed licensing information and use the data accordingly.**

- This dataset is provided **for academic research purposes only and may not be used for commercial purposes**.

- If you use this dataset in your research, please cite our paper.

---

## Data Examples

### Text

#### Medical Assertions

```bash
# Surgery_Schwartz_6744

[
    "Core tasks of the certifying examination have been studied as predictors of clinical performance.", 
    "Proficiency-based training can increase pass rates on the Fundamentals of Laparoscopic Surgery to 100%.", 
    "The Fundamentals of Endoscopic Surgery certification includes the use of a virtual reality flexible endoscopy simulator.", 
    "Procedure-specific simulation provides opportunities to practice and evaluate surgical skills.", 
    "Simulation trainers focus on both bedside procedures and complex surgical procedures.", 
    "Current simulation technologies include virtual reality, physical models, and hybrid models.", 
    "There is a need for efficient, cost-effective, and anatomically accurate models in surgical training.", 
    "Three-dimensional printing has been explored for creating surgical simulation models with varying degrees of success.", 
    "Advancements in printing materials and technologies are expected to increase the use of 3D printing in procedure-specific simulations."
]
```

#### Retrieval Cues

```bash
[
    "What have core tasks of the certifying examination been studied as predictors of in clinical performance?", 
    "What is the maximum pass rate that proficiency-based training can achieve on the Fundamentals of Laparoscopic Surgery?", 
    "What technology is included in the Fundamentals of Endoscopic Surgery certification to enhance technical skill assessment?", 
    "What type of simulation provides valuable opportunities to practice and evaluate essential surgical skills?", 
    "What types of procedures do simulation trainers primarily focus on?", 
    "What are the current simulation technologies mentioned in the reference text?", 
    "What specific needs exist in the field of surgical training regarding model fabrication?", 
    "What technology has been explored for creating surgical simulation models, as mentioned in the reference text?", 
    "What is expected to increase the use of 3D printing in procedure-specific simulations according to advancements in printing materials and technologies?"
]
```

#### A citable evidence snippet

```json
Core tasks of the certifying examination have been extensively studied as both training curriculum components and predictors of clinical performance. Recent research indicates that specific proficiency-based training can elevate pass rates on the Fundamentals of Laparoscopic Surgery (FLS) to 100%, reinforcing the advantages of this training model. Similarly, the Fundamentals of Endoscopic Surgery (FES) certification, which includes a virtual reality simulator for flexible endoscopy, serves to enhance technical skill assessment. Procedure-specific simulation provides valuable opportunities to practice and evaluate essential surgical skills, bridging the gap between basic and complex technical abilities alongside surgical decision-making. While many simulation trainers concentrate on bedside procedures like central venous catheter placement and intubation, some are specifically designed for more intricate operations, including laparoscopic ventral hernia repair and robotic nephrectomy. Currently, simulation technologies encompass virtual reality, physical models, and hybrid models, each offering unique benefits. However, there is a pressing need for cost-effective fabrication methods that yield anatomically accurate models with realistic tissue properties. Several research groups are investigating the potential of three-dimensional (3D) printing for creating surgical simulation models, achieving varying levels of success. As advancements in printing materials and technologies continue to improve, the integration of 3D printing into procedure-specific simulations is expected to grow significantly, enhancing surgical training overall.
```


### Visual

#### Image

<p align="center"> <img src="Visual/80/Image.jpg" alt="Example medical image" width="300"> </p>

#### Findings

```json
{
    "findings": " Increased opacities is seen in the left lower lung base with left lung volume loss is concerning for aspiration. The right lung appears clear. The heart size is unchanged. No pneumothorax. ", 
    "impression": "Increased left lower lung opacities are concerning for aspiration."
}
```

#### Medical Assertions

```json
[CXR][][Lung][left lower base][Opacity][increased][present][certain]  
[CXR][][Lung][left][Volume loss][][present][certain]  
[CXR][][Lung][left][Aspiration concern][][present][possible]  
[CXR][][Lung][right][Opacity][][absent][certain]  
[CXR][][Heart][][Cardiac size][unchanged][present][certain]  
[CXR][][Pleura][][Pneumothorax][][absent][certain]
```

#### Retrieval Cues

```json
Is there an increased opacity in the left lower lung base, and if so, what is its significance in terms of possible aspiration?
Is there evidence of volume loss in the left lung, and if so, what is the likely cause?
Is there a concern for aspiration in the left lung, and if so, where is it located?
Is there an opacity in the right lung on the chest X-ray?
What is the status of the cardiac size in this chest X-ray?
Is there evidence of pneumothorax in the pleura?
```

## MecQA

The in-domain test set is available at:

dataset/MecQA.jsonl