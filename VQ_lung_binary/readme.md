# V/Q Lungs AI Model
- binary model for perfusion and ventilation
- the names of folder **must be used** in the configuration class of the Python script -> comments are present
- the dataset structure for perfusion and ventilation should be 
  - ROOT_FOLDER
    - ABNORMAL
      - train
        - PAT1
          - files in order 01_filename.png, 02_filename.png
        - PATN
      -validation
        - PAT1
        - PATN
    - NORMAL
      - train
        - PAT1
          - files in order 01_filename.png, 02_filename.png
        - PATN
      - validation
        - PAT1
        - PATN
- The perfusion and ventilation dataset must be in separate zip files and also trained separatly
- The dataset creation logic will read this and load the picture in correct order so a quasi SPECT is created.
- **IMPORTANT** It is also necessary to provide the data for evaluation in the same format as for training



