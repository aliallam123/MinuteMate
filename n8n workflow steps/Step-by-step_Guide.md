# Welcome to the Step-by-step guide on how I set up the n8n workflow for MinuteMate

### Step 1: Add the first node - trigger

Add a webhook as the first node, renamed it to 'Meeting Start Trigger.'

This node simulates the start of a meeting (e.g., from Zoom or Teams)
![image](https://github.com/user-attachments/assets/c7db5350-70de-469d-bf4a-dcee7d4c54ac)

### Step 2: Add Audio Capture Node

Add the Code snippet node (formely known as function) and use these settings:
![image](https://github.com/user-attachments/assets/2a04d3dc-5621-4c42-85af-d593b45a6d92)
The code that I inputted simulates live meeting audio input for testing the MinuteMate workflow. Just leave the node not attached to anything for now and move on to step 3

### Step 3: Audio segmentation node

Add another Code snippet node with this code in:
![image](https://github.com/user-attachments/assets/1567fb46-81c6-4392-a1e2-18d7dbf4a0fa)
This node simulates splitting the audio stream into smaller chunks for downstream processing.
