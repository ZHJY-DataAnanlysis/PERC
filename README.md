# <div align="center">📝EduMix-24 and EduMath-24 Datasets

<div align="center">
  <a href="https://huggingface.co/papers/2210.08836"> <img alt="Static Badge" src="https://img.shields.io/badge/HuggingFace-Paper-FFBF00?logo=HuggingFace&logoColor=rgb&labelColor=gray"></a>
  <a href="./LICENSE"> <img alt="Static Badge" src="https://img.shields.io/badge/License-GPLv3-008844?logo=GNUBash&logoColor=rgb&labelColor=gray"></a>
<p></p>

<b>PERC: A Prior-Guided Framework for Classifying Long-Content Educational Resources with Imbalanced Category Distributions</b> </a>

<b>The Conference on Information and Knowledge Management (CIKM) , 2025</b>

:star:Official release of the EduMix-24 and EduMath-24 Datasets.
</div>

## Directory

- [Usage & Download](#usage&download)
- [Description](#description)
- [Collection](#collection)
- [Responsible Use](#responsible-use)
- [Experimental Result](#experimental-result)
- [License](#license)
- [Directory Format](#directory-format)
- [Copyright](#copyright)

## <div align="center" id="usage&download">🖥️Usage & Download</div> <!-- omit in toc -->

- The MSDS dataset can only be used for non-commercial research purposes. For scholar or organization who wants to use the MSDS dataset, please first fill in this [Application Form](./application-form/Application-Form-for-Using-MSDS.docx) and sign the [Legal Commitment](./application-form/Legal-Commitment.docx) and email them to us. When submitting the application form to us, please list or attached 1-2 of your publications in the recent 6 years to indicate that you (or your team) do research in the related research fields of handwriting verification, handwriting analysis and recognition, document image processing, and so on. 
- We will give you the download link and the decompression password after your application has been received and approved.
- All users must follow all use conditions; otherwise, the authorization will be revoked.

## <div align="center" id="description">📖Description</div>

The EduMix-24 and EduMath-24 datasets are specialized collections of educational resources designed for the task of automatic educational content classification.
Here are their key characteristics:

    Source: They were sourced from a real-world intelligent education platform, meaning the data is authentic and reflects modern digital learning materials.

    Composition: Together, they consist of 18,799 individual educational resources. These resources could include items like lesson plans, video lectures, interactive exercises, homework assignments, or presentation slides.

    Annotation: A crucial feature is that all resources have been manually annotated by human experts. This ensures high-quality labels for training and evaluating machine learning models.

    Classification Tasks: The resources are labeled across three distinct classification tasks:

        9 Lesson Types: Categorizing the overall structure or goal of the lesson (e.g., Practice class, Self-study class, Cooperative class).

        15 Teaching Modes: Identifying the primary instructional method used (e.g., Single-point teaching, Heuristic teaching,  Debate teaching).

        9 Activity Elements: Labeling the specific interactive components within the resource (e.g., Identify (A1), Understand (A2), Apply (A3)).

The contributions of MSDS include:

- [x] MSDS-ChS is the largest publicly available Chinese signature dataset for signature for signature verification, at least eight times larger than existing ones.
- [x] MSDS-TDS is the first dataset that covers Token Digit String, which brings a new and effective biometric for handwriting verification.
- [x] The experimental results indicates that the Token Digit String is more powerful than Chinese signature, which is inspiring and promising.

## <div align="center" id="collection">🧬Collection</div> <!-- omit in toc -->

The data of MSDS was acquired with two types of Android tablets. Both of them have specific stylus. We specifically developed an Android app and the user interface is shown below. Users directly performed handwriting on the tablets with specific styluses and the produced information was automatically recorded by the app.

![gui](./images/gui.png)

The data acquisition process is divided into two separate sessions with a time interval of at least 21 days. In each session, users performed writing according to the same procedure: 10 genuine signatures→10 genuine phone numbers→10 forged signatures→10 forged phone numbers.

## <div align="center" id="responsible-use">⚒️Responsible Use</div> <!-- omit in toc -->

MSDS is collected for handwriting identity verification. Specifically, the MSDS-ChS subset could be exploited in online/offline Chinese signature verification, and the MSDS-TDS subset is intended to be used in online/offline identity verification with Token Digit Strings. In addition, MSDS can be exploited in writer identification.

## <div align="center" id="experimental-result">🔭Experimental Result</div> <!-- omit in toc -->

![chs](./images/chs-tds.png)

Experimental results show all models perform better on MSDS-TDS than MSDS-ChS. This finding is inspiring that the accuracy of TDS verification is higher than that of Chinese signature verification as the two subsets were collected simultaneously. Therefore, Token Digit String could be a more effective biometric trait than Chinese signature for high-accurate online verification.

## <div align="center" id="license">📄License</div>

MSDS should be used and distributed under [Creative Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0) License](https://creativecommons.org/licenses/by-nc-nd/4.0/) for non-commercial research purposes.

## <div align="center" id="directory-format">📁Directory Format</div> <!-- omit in toc -->

The dataset is organized in the following directory format:

```bash
├─MSDS
│  ├─MSDS-ChS
│  │  ├─session1
│  │  │  ├─0
│  │  │  │  ├─images
│  │  │  │  │  ├─f_0_0.png
│  │  │  │  │  ├─f_0_1.png
│  │  │  │  │  ├─...
│  │  │  │  │  ├─g_0_0.png
│  │  │  │  │  ├─g_0_1.png
│  │  │  │  │  └─...
│  │  │  │  └─series
│  │  │  │  │  ├─f_0_0.txt
│  │  │  │  │  ├─f_0_1.txt
│  │  │  │  │  ├─...
│  │  │  │  │  ├─g_0_0.txt
│  │  │  │  │  ├─g_0_1.txt
│  │  │  │  │  └─...
│  │  │  ├─1
│  │  │  │  ├─images
│  │  │  │  │  ├─f_0_0.png
│  │  │  │  │  ├─f_0_1.png
│  │  │  │  │  ├─...
│  │  │  │  │  ├─g_0_0.png
│  │  │  │  │  ├─g_0_1.png
│  │  │  │  │  └─...
│  │  │  │  └─series
│  │  │  │  │  ├─f_0_0.txt
│  │  │  │  │  ├─f_0_1.txt
│  │  │  │  │  ├─...
│  │  │  │  │  ├─g_0_0.txt
│  │  │  │  │  ├─g_0_1.txt
│  │  │  │  │  └─...
│  │  │  └─...
│  │  └─session2
│  │      ├─...
│  └─MSDS-TDS
│  │  ├─session1
│  │  │  ├─0
│  │  │  │  ├─images
│  │  │  │  │  ├─f_0_0.png
│  │  │  │  │  ├─f_0_1.png
│  │  │  │  │  ├─...
│  │  │  │  │  ├─g_0_0.png
│  │  │  │  │  ├─g_0_1.png
│  │  │  │  │  └─...
│  │  │  │  └─series
│  │  │  │  │  ├─f_0_0.txt
│  │  │  │  │  ├─f_0_1.txt
│  │  │  │  │  ├─...
│  │  │  │  │  ├─g_0_0.txt
│  │  │  │  │  ├─g_0_1.txt
│  │  │  │  │  └─...
│  │  │  ├─1
│  │  │  │  ├─images
│  │  │  │  │  ├─f_0_0.png
│  │  │  │  │  ├─f_0_1.png
│  │  │  │  │  ├─...
│  │  │  │  │  ├─g_0_0.png
│  │  │  │  │  ├─g_0_1.png
│  │  │  │  │  └─...
│  │  │  │  └─series
│  │  │  │  │  ├─f_0_0.txt
│  │  │  │  │  ├─f_0_1.txt
│  │  │  │  │  ├─...
│  │  │  │  │  ├─g_0_0.txt
│  │  │  │  │  ├─g_0_1.txt
│  │  │  │  │  └─...
│  │  │  └─...
│      └─session2
│  │      ├─...
```

- The `MSDS-ChS` folder contains Chinese signatures and `MSDS-TDS` contains Token Digit Strings (TDS).
- Each of them contains the data in two sessions which is stored in `session1` and `session2`.
- The users are arranged from `0` to `401`, with online dynamic time series and offline static images provided in `series` and `images`. The time series are saved as `.txt` files and the images are in `.png` format.
- The naming of each file follows the same format: `flag_user_index`.
- - `flag` is `f` or `g`. `f` indicates that this file is a skilled forgery, while `g` indicates that it is a genuine sample.
- - `user` indicates the number of user of this file.
- - `index` indicates the number of this file (`.txt` or `.png`) in the current folder.
- - For example, `f_0_0.txt` represents the first file (time series) of all skilled forgeries of the user `0`. `g_5_6.png` represents the seventh file (image) of all genuine samples of the user `5`.

## <div align="center" id="citation">:bookmark_tabs:Citation</div> <!-- omit in toc -->

```
@inproceedings{zhang2022msds,
    author = {Zhang, Peirong and Jiang, Jiajia and Liu, Yuliang and Jin, Lianwen},
    booktitle = {{Advances in Neural Information Processing Systems (NeurIPS)}},
    pages = {36507--36519},
    title = {{MSDS: A Large-Scale Chinese Signature and Token Digit String Dataset for Handwriting Verification}},
    volume = {35},
    year = {2022}
}
```

## <div align="center" id="copyright">:palm_tree:Copyright</div> <!-- omit in toc -->

For commercial purpose usage, please contact Prof. Lianwen Jin: eelwjin@scut.edu.cn.

Copyright 2022-2025, [Deep Learning and Vision Computing Lab](http://www.dlvc-lab.net), South China China University of Technology.



