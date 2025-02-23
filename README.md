# Classification of Drusen, DME and CNV OCT images using Deep Learning algorithms

## Introduction:
In contemporary times, there has arisen a burgeoning apprehension concerning retinal ailments, which have surfaced as a notable public health concern. These maladies progress incrementally and often elude detection due to the absence of overt symptoms. According to National Library of Medicine, 2.2 Million people globally are suffering from Vision Impairments, can grow to 5.4 million by 2050. These disorders can manifest in diverse presentations, primarily impacting visual function. They can afflict any segment of the retina, resulting in visual impairments and, in severe instances, blindness. Examples of retinal disorders encompass diabetic retinopathy, macular pucker, glaucoma, macular hole, age-related macular degeneration, drusen, central serous retinopathy, macular edema, vitreous traction, and abnormalities of the optic nerve.

The human eye is an intricate organ tasked with the process of vision, comprising several constituent elements that collaborate harmoniously to capture and interpret light. Its principal components encompass the cornea, iris, pupil, lens, retina, and optic nerve. Positioned at the posterior aspect of the eye, the retina assumes paramount importance, housing light-sensitive cells known as photoreceptors that transmute light into electrical impulses. Within the retina lies the macula, a diminutive region centrally situated, pivotal in facilitating acute, focal vision vital for tasks such as reading and driving. The retina assumes a pivotal function in receiving and structuring visual stimuli. **Early detection and treatment are essential to prevent vision loss.** 

Optical Coherence Tomography (OCT) stands as a pivotal diagnostic instrument, delivering high-fidelity imaging and precise quantification of retinal layers impacted by pathology. Leveraging light waves, OCT generates cross-sectional retinal images, furnishing intricate details crucial for diagnostic discernment and continual monitoring of retinal and optic nerve alterations over time. This technological advancement assumes paramount significance in ensuring precise diagnosis and optimal selection of therapeutic interventions. Ophthalmologists harness OCT's capabilities to meticulously inspect each stratum of the retina, facilitating mapping and evaluation of their thickness, thereby enhancing diagnostic efficacy. These quantitative metrics not only bolster the diagnostic process but also inform therapeutic strategies for conditions like glaucoma and retinal pathologies. OCT finds utility in diagnosing an array of ocular disorders. Traditional classification methodologies for retinal ailments have exhibited accuracies ranging from 80% to 91%. Consequently, a sophisticated deep learning framework predicated on convolutional neural networks has been devised to enhance the precision of retinal disease classification, particularly in the nascent stages of pathology.

<p align="center">
   <img width="617" alt="image" src="https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/a90fe410-a320-4bc6-9a3f-96273e0b7100">
</p>

1. Drusen, characterized as diminutive yellow accumulations beneath the retina, primarily in the macular region, are effectively visualized using OCT images. This capability aids eye care specialists in identifying age-related macular degeneration (AMD), a prominent cause of vision impairment in the elderly population.

2. Diabetic macular edema (DME) emerges as a complication of diabetic retinopathy, prevalent among individuals with diabetes. OCT proves indispensable in diagnosing DME by delineating macular edema resulting from fluid leakage originating from blood vessels.

3. Choroidal neovascularization (CNV) denotes the abnormal growth of blood vessels beneath the retina. Utilizing OCT imaging, CNV can be detected through the visualization of these anomalous vessels and any associated fluid or hemorrhagic leakage.

In essence, OCT plays a pivotal role in the identification and therapeutic management of ocular conditions like drusen, DME, and CNV. By furnishing detailed retinal images, OCT empowers eye care practitioners to accurately diagnose these conditions and formulate tailored treatment regimens to safeguard visual acuity.

<p align="center">
    <img width="750" alt="image" src="https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/209848c1-0d9a-49c7-b149-cf6c7f877e59">
</p>

## Dataset:

The dataset used in this project is obtained from Mendeley(https://data.mendeley.com/datasets/rscbjbr9sj/3) and it contains OCT images of retinas. It consists of a total of **62138 images** , categorized into the following classes:
- CNV (Choroidal Neovascularization)
- DME (Diabetic Macular Edema)
- DRUSEN
- NORMAL

The distribution of data is as below:
1. NORMAL - 26565
2. CNV - 15109
3. DME - 11598
4. DRUSEN - 8866

<p align="center">
   <img width="900" alt="image" src="https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/d87ef1e2-bb5a-4d5d-90b6-647c7f5d4671">
</p>

## Preprocessing steps were undertaken as follows:

1. The images were resized uniformly to dimensions of 256x256 pixels.
2. Subsequently, normalization was applied to scale the pixel values within the range of 0 to 1.
3. Augmentation techniques were employed using the following parameters within the defined data augmentation process:
   - Rotation range: 10 degrees
   - Width shift range: 0.1 (10% of the image width)
   - Height shift range: 0.1 (10% of the image height)
   - Shear range: 0.1 (10% shear intensity)
   - Zoom range: 0.1 (zooming range of 10%)
   - Horizontal flip: Enabled (random horizontal flipping)
   - Vertical flip: Enabled (random vertical flipping)
   - Fill mode: Nearest neighbor interpolation to handle pixel filling near boundaries.

_We have experimented with various models as outlined in the Python file attached to this project. The F-1 scores for both the training and testing datasets for all the models are presented in the table below._

<p align="center">
   <img width="650" alt="image" src="https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/dd35ff01-382b-411b-9bed-803f28d0cd7c">
</p>

The CNN model below demonstrates superior performance compared to all other algorithms.

<p align="center">
   <img width="650" alt="image" src="https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/d00cc775-74c5-4aa6-b863-53565493eae5">

   <img width="896" alt="image" src="https://github.com/hemanth08/OCT_ImageClassification/assets/102893567/f58dc72c-107b-4690-ab15-736311ac2118">
</p>

Contact Information:
•	Hemanth Varma Dantuluri (h167@umbc.edu)
•	Satyasai Mandlem(satyasm1@umbc.edu)
•	Nikitha Guntaka
