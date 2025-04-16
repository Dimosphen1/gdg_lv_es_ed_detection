# GDG LV ES ED detection

## Installation
1. Clone the repository to an empty directory:
    ```shell
    git clone https://github.com/Dimosphen1/gdg_lv_es_ed_detection.git .
    ```
2. Create and activate the virtual environment (python 3.11.9 will be used during the demo):
    ```shell
    python -m venv venv
    ```
- On Mac/Linux:
    ```shell
    source venv/bin/activate
    ```
- On Windows:
    ```shell
    venv\Scripts\activate
    ```
3. Install the requirements from the `requirements.txt` file:
    ```shell
    pip install -r requirements.txt
    ```
4. Install PyTorch [following the instructions](https://pytorch.org/get-started/locally/#start-locally) (The CUDA 12.6 compute platform is preferred if available).
5. Download the [EchoNet-Dynamic](https://stanfordaimi.azurewebsites.net/datasets/834e1cd1-92f7-4268-9daa-d359198b310a) dataset. If you encounter any difficulties, please refer to the [Notes](#detailed-echonet-dynamic-download-steps) section.
6. Place the `FileList.csv` in the `data\file_list` directory from the repository.
7. Place files from the `Video` directory from the `EchoNet-Dynamic` dataset to the `data\videos` directory from the repository.
8. Start the jupyter lab and open `start.ipynb`:
    ```shell
    jupyter lab .\start.ipynb
    ```
9. Execute first two cells, the output of the second cell should be:
    ```
    file_list_present=True
    video_content_count=10032
    ```
10. Congratulations! You have successfully completed the initial setup.

## Notes
### Detailed `EchoNet-Dynamic` download steps
1. Open `EchoNet-Dynamic` [dataset link](https://stanfordaimi.azurewebsites.net/datasets/834e1cd1-92f7-4268-9daa-d359198b310a)
2. Click the `login` button in the `Export Dataset` section;
3. Sign in using your Microsoft account. Create one if you do not have an account.
4. After logging in, press `Download (7.04 GB)` button.
5. Copy the download link.
6. Download and install [Azure Storage Explorer](https://azure.microsoft.com/en-us/products/storage/storage-explorer/#Download-4).
7. Open Azure Storage Explorer.
8. Select `Connect to the resource`.
9. Select `Container or BLOB-objects catalog`.
10. Select `Signed URL-address (SAS)`.
11. Paste the download link to the `URL-adress of the SAS container or BLOB-objects catalog`.
12. Press `Next` (Displayed name should include `echonetdynamic`).
13. Follow the remaining instructions to complete the dataset download.
