# oral-cancer
Stain Deconvolution for Deep Learning Based Multiclass Diagnosis of Oral Cancer in Liquid-Based Cytology

PAPER: LINK

ABSTRACT
Background: Oral cancer remains a major public health challenge, with prognosis and survival rates highly dependent on early detection
and accurate diagnosis. While conventional diagnosis relies on invasive tissue biopsies and histological examination, these approaches can
be resource-intensive, time-consuming, and impractical for routine screening or continuous monitoring of at-risk populations. Liquid-based
cytology (LBC) combined with Papanicolaou staining provides a non-invasive, cost-effective alternative that enables large-scale screening
of oral mucosal cells. However, accurate interpretation of cytological slides still depends heavily on expert pathologists, and the absence
of detailed cell-level annotations limits the development and evaluation of reliable AI-based diagnostic tools. This study aims to improve
AI-assisted oral cancer detection by introducing additional diagnostic information through stain deconvolution and systematically comparing
the performance of deep learning models trained on original RGB images and stain-separated channels. By leveraging targeted stain
information, the proposed approach seeks to enhance classification accuracy and interpretability, supporting more robust and scalable
computer-assisted screening for early oral cancer detection.
Methods: We analyze H&E-stained liquid-based cytology (LBC) slides using a convolutional neural network trained on both original
RGB images and stain-separated channels (Haematoxylin, Eosin, and DAB) extracted via color deconvolution. The dataset comprises 962
digitized LBC images spanning four diagnostic classes (NILM, LSIL, HSIL, SCC). Images are preprocessed with resizing, normalization, and
augmentation to enhance model generalizability. Given the absence of detailed cytological annotations, we adopt a fully supervised deep
learning approach using only image-level diagnostic labels. Model performance is evaluated using a stratified 4-fold cross-validation, with
metrics including F1 score, accuracy, recall, precision, and ROC AUC. Statistical comparisons between models are conducted using the
Friedman test with Conover’s post hoc analysis (Holm correction) to assess the impact of stain separation. Grad-CAM visualizations are
generated to interpret the discriminative regions contributing to classification decisions.
Results: Our experiments demonstrate that: (i) the DAB stain-deconvoluted channel consistently yields the highest diagnostic performance
among all tested configurations, achieving an F1 score of 95.8% and an accuracy of 98.2%, with improved true positive detection and fewer
false negatives for clinically significant classes; (ii) the Eosin channel provides significantly different but weaker diagnostic information
compared to RGB and other channels (p < 0.05, Conover’s post hoc test), underscoring its limited contribution when used in isolation. Thus,
stain deconvolution offers valuable complementary diagnostic information beyond conventional RGB imaging, supporting its utility for
improving the reliability and interpretability of automated oral cancer classification.
Conclusion: This pilot study advances automated oral cytology by integrating deep learning with stain deconvolution to improve the
multi-class classification of liquid-based Pap smear images. Our results show that targeted stain separation, particularly isolating the DAB
channel, can significantly enhance diagnostic performance by improving true positive detection rates and reducing false negatives for
high-grade lesions and carcinoma, which are critical for early intervention. This approach demonstrates that leveraging complementary
stain information can increase the reliability and interpretability of AI-assisted cytological screening without adding unnecessary complexity
to the laboratory workflow. Moreover, this framework has broader potential for adaptation to immunocytochemistry applications, where
alternative staining protocols could similarly be optimized to support more accurate and explainable automated diagnosis
