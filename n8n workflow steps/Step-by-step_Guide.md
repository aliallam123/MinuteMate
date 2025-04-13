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

### Step 4: Context Preprocessing Node

This node will connect to the previous node.
![image](https://github.com/user-attachments/assets/d160c4e7-85bd-4a0b-83f8-6dfdd811fb4c)
This node takes each audio chunk and appends a “[cleaned]” tag to simulate preprocessing (e.g., removing filler words or identifying speakers).

Now your workflow should look like this:
![image](https://github.com/user-attachments/assets/d3b7cd00-a81a-4b63-ad92-eec5942a7e3b)

