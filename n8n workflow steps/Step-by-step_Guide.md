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

### Step 5: Emotion Detection Node

This step simulates sending each cleaned audio segment to an emotion analysis API and getting back a mood label (e.g., "neutral", "laughing", "serious").

Add another code snippet node, use this code:
![image](https://github.com/user-attachments/assets/fd7b6a7a-f250-45ca-baeb-1460bee178c3)
This code adds a simulated emotional label (e.g., “neutral”) to each cleaned segment to support tone-aware meeting summaries.

#### At this point, all nodes should be connected except the first 'meeting start trigger node' because we are simulating inputs manually right now (not calling real APIs).

Audio Capture is your first test node to generate dummy data.

Now, your workflow should look like this:
![image](https://github.com/user-attachments/assets/bca241d7-dbe1-4c49-b177-96e4174348d3)

### Step 6: AI Summary Generator

This is where we simulate sending the cleaned + emotion-tagged segments to GPT or Claude for summarisation.

Add this code:
![image](https://github.com/user-attachments/assets/aaef7c37-ae1d-409b-b1f6-b71cc8de8321)

Now connect to the previous node:
![image](https://github.com/user-attachments/assets/d26ffafd-f003-4e19-bc20-9d89e68bb559)

### Step 7: Encrypt Output Node

This node mimics encrypting the final summary for secure delivery or storage.
![image](https://github.com/user-attachments/assets/82e9a0a3-583c-436a-bd7c-a2b61ab18a6c)
Add the code and connect the node to the previous one and move onto the next step.

### Step 8: Deliver Summary Node

This node simulates sending the encrypted summary to a stakeholder e.g., via email, Slack, or document storage.
![image](https://github.com/user-attachments/assets/b6e94502-44f7-44bb-ae7c-2bd9e0f90217)

Now to test we need to resolve two issues:

1. The First Meeting Start Trigger node is not connected so the workflow won't run

2. The last node does not finish/not connected to anything

How to resolve both issues:

1. Simply connect the First node (Meeting Start Trigger) to the Second node (Audio Capture) now by dragging the grey circle on the first node to the second

2. You don’t need to manually “close” it just make sure It's the final node in the chain

Now the workflow is ready to run! Let's click 'Test Workflow' and see what happens:
![image](https://github.com/user-attachments/assets/6ff774f6-afca-4681-9c28-9c8eceb51f25)
![image](https://github.com/user-attachments/assets/0f1736a9-c067-4d9e-a20a-ec964720b824)
### Success!
