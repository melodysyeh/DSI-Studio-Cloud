# DSI Studio Automated Tracking on GITHUB

This repository runs DSI Studio's atuomated tracking using Github Action, which offers 20 concurrent jobs with 2-core CPU each, equivalent to a 40-core workstation. 

**The data will be publicly accessibile by everyone. Do not use this to process patient or sensitive data.**

The process takes a **FIB file** as the input data [(steps to generate a FIB file from NIFTI or DICOM files)](https://dsi-studio.labsolver.org/doc/gui_t1.html)

## Steps

1. Fork the repository: Click on the `Fork` button in the upper right corner.

<img src="https://user-images.githubusercontent.com/275569/157118034-8a28b553-fa86-4a5c-a542-b65b36793c63.png" width=400>

2. Click on the `Actions` menu and confirm `I understand my workflows, go ahead and enable them`. Now you have the automated fiber tracking enabled.
3. Under the same `Actions` menu, click on `Automated fiber tracking` on the left and click run `workflow` on the right.

<img src="https://user-images.githubusercontent.com/275569/157118122-cca1dc7f-4767-43f7-b450-f73744ca3934.png" width=400>

4. Input the URL for the FIB file starting with (e.g.,  https://zenodo.org/record/6307812/files/100206.src.gz.gqi.1.7.fib.gz ) and click on `Run workflow` to start tracking.
5. The tracking will take a while to start and complete. You can cancel it at any time, and partial results will still be saved.
6. The output will be saved under `Artifacts` as a zip file named tractography

<img src="https://user-images.githubusercontent.com/275569/157118239-969e137a-f103-47ed-a1b9-fe6d134fc2e4.png" width=400>




