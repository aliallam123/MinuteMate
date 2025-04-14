# This is how to test the workflow we made (in Set-up-Guide.md) with Actual Data

### Step 1: Go to your workflow:

![image](https://github.com/user-attachments/assets/955b0280-2f94-4bab-b077-c4c191012cff)
Click the Meeting Start Trigger

You will see a Test URL custom to YOU, I will not show mine but copy the URL:
![image](https://github.com/user-attachments/assets/1a4879be-df90-4e87-9fe6-2e52ca18c45a)

### Step 2: Send Data Using Postman (or curl)

VERY IMPORTANT - go on Meeting Start Trigger node and set HTTP method from GET to POST

Copy that URL and paste it in a browser

and at this at the end of the browser:

?audio=This is a live test from Ali to simulate a real meeting summary.

Hit Enter.

Go back to n8n, open the Executions tab at the top.

Click the latest execution to view the workflow run.

### Step 3: Use Real Webhook Data Instead of Mock Output

Change the code for the Audio Capture Node to this:

const input = $json.audio || "No audio input received";
return [{ json: { audio: input } }];

This grabs whatever ?audio=... value is passed from the webhook.

Changing the Audio Capture node to use webhook input does not break your workflow - it upgrades it to support both testing and real data.

This gives you real webhook input if it exists, but falls back to fake data if nothing is sent.

Now test workflow again
![image](https://github.com/user-attachments/assets/c85b2ef2-2eb6-4423-b7db-21a860f12ae8)
