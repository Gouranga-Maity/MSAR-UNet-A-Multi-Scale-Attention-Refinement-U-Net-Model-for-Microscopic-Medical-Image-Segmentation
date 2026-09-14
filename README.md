# MSAR-UNet-A-Multi-Scale-Attention-Refinement-U-Net-Model-for-Microscopic-Medical-Image-Segmentation

Abstract:  Automatic and accurate nuclei segmentation in histopathol-
ogy images is a fundamental task in computational pathology, yet it
remains highly challenging due to complex nuclear morphologies, vari-
ations in shape, size, and staining intensity, and frequent overlaps be-
tween nuclei. This paper proposes MSAR-UNet, a Multi-Scale Attention
Refinement U-Net, which couples two complementary modules within
a standard encoder–decoder backbone. A Multi-Scale Dilated Residual
Block (MSDRB) is embedded in the encoder to jointly capture local,
intermediate, and large-scale contextual information through parallel
standard and dilated convolutional branches with residual feature prop-
agation. A Channel-Spatial Skip Refinement Module (CSSRM) is in-
troduced along the skip connections to adaptively recalibrate encoder
features via complementary channel and spatial-attention maps, sup-
pressing less discriminative responses prior to decoder fusion. Extensive
experiments on four publicly available histopathology datasets, namely
MoNuSeg, TNBC, CoNSeP and DDT1, our model demonstrate consis-
tent improvements over the U-Net baselines and several state-of-the-art
methods. MSAR-UNet achieves Dice scores of 80.69%, 83.48%, 77.26%,
and 85.97%, with corresponding IoU scores of 67.66%, 71.65%, 62.94%,
and 75.58% on MoNuSeg, TNBC, CoNSeP, and DDT1, respectively. 

<img width="2000" height="1125" alt="overall_Final_v3-1" src="https://github.com/user-attachments/assets/02fa2fb4-c695-44b0-b481-9bdd10d479e3" />
# Channel-Spatial Skip Refinement Module (CSSRM)

<img width="2162" height="402" alt="CSSRM_V1_cropped-1" src="https://github.com/user-attachments/assets/7c4805fc-4fa4-4240-a7e1-62bf15204f14" />
# Multi-Scale Dilated Residual Block (MSDRB)
<img width="2731" height="798" alt="MSDRB-1" src="https://github.com/user-attachments/assets/3996a742-f6d6-4386-b228-c762de996dfa" />

# Dataset Description
<table>
<thead>
<tr>
<th>Dataset</th>
<th>Modality</th>
<th>Organ</th>
<th>Images</th>
<th>Magnification</th>
<th>Resolution</th>
</tr>
</thead>
<tbody>
<tr>
<td>MoNuSeg</td>
<td>Microscopic</td>
<td>7</td>
<td>51</td>
<td>40×</td>
<td>1000 × 1000</td>
</tr>
<tr>
<td>TNBC</td>
<td>Microscopic</td>
<td>1</td>
<td>50</td>
<td>40×</td>
<td>512 × 512</td>
</tr>
<tr>
<td>ConSeP</td>
<td>Microscopic</td>
<td>1</td>
<td>41</td>
<td>40×</td>
<td>1000 × 1000</td>
</tr>
<tr>
<td>DDT1</td>
<td>Ultrasound</td>
<td>1</td>
<td>637</td>
<td>–</td>
<td>380 × 420</td>
</tr>
</tbody>
</table>

# Model Ablation Table
<table>
<tr>
<th rowspan="2">Model Configuration</th>
<th colspan="2">MoNuSeg</th>
<th colspan="2">TNBC</th>
<th colspan="2">CoNSeP</th>
<th colspan="2">DDT1</th>
</tr>
<tr>
<th>Dice</th>
<th>IoU</th>
<th>Dice</th>
<th>IoU</th>
<th>Dice</th>
<th>IoU</th>
<th>Dice</th>
<th>IoU</th>
</tr>

<tr>
<td>U-Net</td>
<td>75.47</td>
<td>60.65</td>
<td>82.95</td>
<td>70.86</td>
<td>75.16</td>
<td>60.20</td>
<td>82.32</td>
<td>70.31</td>
</tr>

<tr>
<td>U-Net + MSDRB</td>
<td>80.18</td>
<td>66.95</td>
<td>83.21</td>
<td>71.24</td>
<td>76.05</td>
<td>61.36</td>
<td>85.09</td>
<td>74.38</td>
</tr>

<tr>
<td><b>All (proposed)</b></td>
<td><b>80.69</b></td>
<td><b>67.66</b></td>
<td><b>83.48</b></td>
<td><b>71.65</b></td>
<td><b>77.26</b></td>
<td><b>62.94</b></td>
<td><b>85.97</b></td>
<td><b>75.58</b></td>
</tr>
</table>

# Cross dataset validation 
<h3>Cross-Dataset Validation Results</h3>

<table>
  <thead>
    <tr>
      <th rowspan="2">Training / Validation Dataset</th>
      <th colspan="2">TNBC (Test)</th>
      <th colspan="2">MoNuSeg (Test)</th>
      <th colspan="2">CoNSeP-Binary (Test)</th>
    </tr>
    <tr>
      <th>Dice</th>
      <th>IoU</th>
      <th>Dice</th>
      <th>IoU</th>
      <th>Dice</th>
      <th>IoU</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td><strong>TNBC</strong></td>
      <td>—</td>
      <td>—</td>
      <td>0.6712</td>
      <td>0.5051</td>
      <td>0.6924</td>
      <td>0.5298</td>
    </tr>

   <tr>
      <td><strong>MoNuSeg</strong></td>
      <td>0.7005</td>
      <td>0.5429</td>
      <td>—</td>
      <td>—</td>
      <td>0.7143</td>
      <td>0.5558</td>
    </tr>

   <tr>
      <td><strong>CoNSeP-Binary</strong></td>
      <td>0.6712</td>
      <td>0.5051</td>
      <td>0.6924</td>
      <td>0.5298</td>
      <td>—</td>
      <td>—</td>
    </tr>
  </tbody>
</table>

<p><strong>Note:</strong> Each row represents the dataset used for training and validation, while each column group represents an independent test dataset. The diagonal entries (—) indicate that cross-dataset evaluation was not performed for the same training and test dataset.</p>


# Qualitative Visualization Analysis

<img width="2643" height="915" alt="Finalgradacm_MSAR" src="https://github.com/user-attachments/assets/7c161f19-fa9e-4a9e-ae47-cc3ee29a9d96" />







