# DSI Studio on GitHub Cloud Computing

This repository runs DSI Studio's atuomated tracking using Github Action, which offers 20 concurrent jobs with 2-core CPU each, equivalent to a 40-core workstation. 

**The data will be publicly accessibile by everyone. Do not use this to process patient or sensitive data.**

The process takes a **FIB file** as the input data [(steps to generate a FIB file from NIFTI or DICOM files)](https://dsi-studio.labsolver.org/doc/gui_t1.html)

## Auto-Track using URL

1. Fork the repository: Click on the `Fork` button in the upper right corner.

<img src="https://user-images.githubusercontent.com/275569/157307065-a172c393-a4db-4cf3-92c8-b4482619a0e7.png" width=500>

2. Click on the `Actions` menu and confirm `I understand my workflows, go ahead and enable them`. Now you have the automated fiber tracking enabled. Under the same `Actions` menu, click on `Auto-Track (URL)` on the left and click run `workflow` on the right.

<img src="https://user-images.githubusercontent.com/275569/157307610-5f2e5e9b-ed6f-44e3-b084-6c42f23ac146.png" width=500>


3. Input the URL for the FIB file starting with (e.g.,  https://zenodo.org/record/6307812/files/100206.src.gz.gqi.1.7.fib.gz ) and click on `Run workflow` to start tracking.
4. The tracking will take a while to start and complete. You can cancel it at any time, and partial results will still be saved.
5. The output will be saved under `Artifacts` as a zip file named tractography

<img src="https://user-images.githubusercontent.com/275569/157118239-969e137a-f103-47ed-a1b9-fe6d134fc2e4.png" width=500>


## Auto-Track using OpenNeuro Accession Number

1. Repeat the (1)(2) steps of the Auto-Track URL version

2. Under the `Actions` menu, click on `Auto-Track (OpenNeuro)` on the left and click run `workflow` on the right.

3. Input the OpenNeuro Accession Number (e.g. ds000031) and click on `Run workflow` to start tracking.





