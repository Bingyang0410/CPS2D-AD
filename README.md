# Anomaly Detection of Integrated Circuits Package Substrates Using the Large Vision Model SAIC: Dataset Construction, Methodology, and Application

## Data Link
The dataset is uploaded into Google Drive, and the partial source data can be download in [here](https://drive.google.com/file/d/1Nasd7FhU0hqE7BzhwGm6UevbHMJjP4Ni/view?usp=sharing). The data collection and open-source have been authorized by a resolution of the company's board of directors. However, considering the possibility of data leakage during the review stage, our anonymous GitHub link does not fully cover all the data. If the paper is fortunate enough to be accepted, we will open source all the data samples and annotated files.

## Data Description
The data of CPS2D-AD comes from ceramic packaging substrate samples in actual factory environments. As shown in Figure 1, these samples were selected during the punching hole, filling hole, and printing stage, representing actual production conditions and process changes. To ensure the accuracy and integrity of the data, we design a systematic AOI equipment to ensure the quality of each sample during capture processing.

![Data source](Fig-2.png "Figure 1")

CPS2D-AD contains 6 common types of defect from 40 different product, such as open circuit, mouse bite, overflow, foreign matter, poor pattern, and leakage, the example of each defect can be seen in Figure 2. In the data annotation stage, we utilize Labelme to accurately annotate the defect on the ceramic package substrate surface at pixel and bounding-box levels.

![Details](Fig-4.png "Figure 2")

## Benchmark Construction

"Minimum to maximum usage of data samples and annotations" is the logic to construct our benchmarks. In order to quickly build experiments to validate the effectiveness of the CPS2D-AD dataset, we referred to many excellent open-source frameworks. As for the scenarios without a open-source framework, we replicated these algorithm on our dataset using the corresponding GitHub source code from the references.

In order to provide a more detailed explanation of the problem definitions involved in the tasks in our benchmark, we illustrate the usage of supervision and data by different tasks through Figure 3.

![Problem](Fig-0.png "Figure 3")

### Unsupervised task
We follow the pipeline of [anomalib](https://github.com/openvinotoolkit/anomalib) and [open-iad](https://github.com/M-3LAB/open-iad) to conduct our experiments about unsupervised task.

### Semi-supervised task
We follow the pipeline of [open-iad](https://github.com/M-3LAB/open-iad) to conduct our experiments about semi-supervised task.

### Few-shot task
We have reproduced the few-shot algorithm listed in the paper for CPS2D-AD without referring to other publicly available frameworks. The concrete code used in our benchmark is uploaded in this issue.

### Fully-supervised task
We following the pipeline of [mmsegmentation](https://github.com/open-mmlab/mmsegmentation) to conduct our experiments about fully-supervised task.

## Evaluate your own method
We will publish the relevant evaluation code and evaluate the model online by uploading an Excel file like Kaggle or Ali Tianchi competition.

## Licenses
The dataset is released under the CC BY 4.0 license. All data collection processes are authorized by the relevant companies.

## Citation
'''
@inproceedings{cps2dad,
      title={Anomaly Detection of Integrated Circuits Package Substrates Using the Large Vision Model SAIC: Dataset Construction, Methodology, and Application}, 
      author={Ruiyun Yu and Bingyang Guo and Haoyuan Li},
      year={2025},
      booktitle={{IEEE/CVF} International Conference on Computer Vision, {ICCV} 2025}, 
}
'''
