# DSI Studio on GitHub Cloud Computing

This repository runs DSI Studio's automated tracking using Github Action, which offers 20 concurrent jobs with a 2-core CPU each, equivalent to a 40-core workstation. 

**The data will be publicly accessible by everyone. Do not use this to process patient or sensitive data.**


## Auto-Track on OpenNeuro 

1. Fork the repository: Click on the `Fork` button in the upper right corner.

<img src="https://user-images.githubusercontent.com/275569/157307065-a172c393-a4db-4cf3-92c8-b4482619a0e7.png" width=500>

2. Click on the `Actions` menu and confirm `I understand my workflows, go ahead and enable them`. Now you have automated fiber tracking enabled. Under the same `Actions` menu, click on `Auto-Track (OpenNeuro)` on the left and click run `workflow` on the right.

<img src="https://user-images.githubusercontent.com/275569/157596167-7d9ee687-2633-4d48-ba5f-c12c62b04b35.png" width=500>

3. Assign `OpenNeuro Accession Number` (e.g. ds000031) 

4. Assign `Tract of Interest`

   Support partial name, and multiple tracts can be assigned using comman separator (e.g. Arcuate,Optic_Radiation).

The full list of tracts supported:

```
Arcuate_Fasciculus_L
Arcuate_Fasciculus_R
Cingulum_Frontal_Parahippocampal_L
Cingulum_Frontal_Parahippocampal_R
Cingulum_Frontal_Parietal_L
Cingulum_Frontal_Parietal_R
Cingulum_Parahippocampal_Parietal_L
Cingulum_Parahippocampal_Parietal_R
Cingulum_Parahippocampal_L
Cingulum_Parahippocampal_R
Cingulum_Parolfactory_L
Cingulum_Parolfactory_R
Extreme_Capsule_L
Extreme_Capsule_R
Frontal_Aslant_Tract_L
Frontal_Aslant_Tract_R
Inferior_Fronto_Occipital_Fasciculus_L
Inferior_Fronto_Occipital_Fasciculus_R
Inferior_Longitudinal_Fasciculus_L
Inferior_Longitudinal_Fasciculus_R
Middle_Longitudinal_Fasciculus_L
Middle_Longitudinal_Fasciculus_R
Parietal_Aslant_Tract_L
Parietal_Aslant_Tract_R
Superior_Longitudinal_Fasciculus1_L
Superior_Longitudinal_Fasciculus1_R
Superior_Longitudinal_Fasciculus2_L
Superior_Longitudinal_Fasciculus2_R
Superior_Longitudinal_Fasciculus3_L
Superior_Longitudinal_Fasciculus3_R
Uncinate_Fasciculus_L
Uncinate_Fasciculus_R
Vertical_Occipital_Fasciculus_L
Vertical_Occipital_Fasciculus_R
Acoustic_Radiation_L
Acoustic_Radiation_R
Corticobulbar_Tract_L
Corticobulbar_Tract_R
Corticopontine_Tract_Frontal_L
Corticopontine_Tract_Frontal_R
Corticopontine_Tract_Parietal_L
Corticopontine_Tract_Parietal_R
Corticopontine_Tract_Occipital_L
Corticopontine_Tract_Occipital_R
Corticospinal_Tract_L
Corticospinal_Tract_R
Corticostriatal_Tract_Anterior_L
Corticostriatal_Tract_Anterior_R
Corticostriatal_Tract_Posterior_L
Corticostriatal_Tract_Posterior_R
Corticostriatal_Tract_Superior_L
Corticostriatal_Tract_Superior_R
Thalamic_Radiation_Anterior_L
Thalamic_Radiation_Anterior_R
Thalamic_Radiation_Posterior_L
Thalamic_Radiation_Posterior_R
Thalamic_Radiation_Superior_L
Thalamic_Radiation_Superior_R
Dentatorubrothalamic_Tract_L
Dentatorubrothalamic_Tract_R
Fornix_L
Fornix_R
Medial_Lemniscus_L
Medial_Lemniscus_R
Optic_Radiation_L
Optic_Radiation_R
Reticular_Tract_L
Reticular_Tract_R
Anterior_Commissure
Corpus_Callosum_Forceps_Minor
Corpus_Callosum_Body
Corpus_Callosum_Tapetum
Corpus_Callosum_Forceps_Major
Cerebellum_L
Cerebellum_R
Inferior_Cerebellar_Peduncle_L
Inferior_Cerebellar_Peduncle_R
Middle_Cerebellar_Peduncle
Superior_Cerebellar_Peduncle
Vermis
CNII_L
CNII_R
CNIII_L
CNIII_R
CNV_L
CNV_R
CNVII_L
CNVII_R
CNVIII_L
CNVIII_R
```

5. Click on `Run workflow` to start tracking. The tracking will take a while to start and complete. You can cancel it at any time, and partial results will still be saved.

6. Once the process completed, the FIB files and tract files will be saved. They can be downloaded and viewed in DSI Studio.

<img src="https://user-images.githubusercontent.com/275569/157700442-6fae3601-9208-4607-af56-eb4b44d43877.png" width=500>



## Auto-Track using URL

This process takes a **FIB file** as the input data [(steps to generate a FIB file from NIFTI or DICOM files)](https://dsi-studio.labsolver.org/doc/gui_t1.html)

1. Fork the repository: Click on the `Fork` button in the upper right corner.

<img src="https://user-images.githubusercontent.com/275569/157307065-a172c393-a4db-4cf3-92c8-b4482619a0e7.png" width=500>

2. Click on the `Actions` menu and confirm `I understand my workflows, go ahead and enable them`. Now you have automated fiber tracking enabled. Under the same `Actions` menu, click on `Auto-Track (URL)` on the left and click run `workflow` on the right.

<img src="https://user-images.githubusercontent.com/275569/157307610-5f2e5e9b-ed6f-44e3-b084-6c42f23ac146.png" width=500>

3. **Test the URL on the browser to make sure it downloads a FIB file.** Then input the URL for the FIB file starting with (e.g.,  https://zenodo.org/record/6307812/files/100206.src.gz.gqi.1.7.fib.gz ) and click on `Run workflow` to start tracking. The tracking will take a while to start and complete. You can cancel it at any time, and partial results will still be saved.

4. Once the process completed, the tract files  will be saved under `Artifacts` as a zip file named tractography

<img src="https://user-images.githubusercontent.com/275569/157118239-969e137a-f103-47ed-a1b9-fe6d134fc2e4.png" width=500>



