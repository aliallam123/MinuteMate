# This is how to test the workflow we made (in Set-up-Guide.md) with Real Data (using Hoppscotch)

### Step 1: Recreate the Webhook Node

Delete the old Meeting Start Trigger node.

Add a new Webhook node.

Set method to POST.

Keep the default webhook path or rename it to something like start-meeting.

You’ll now get a test webhook URL like:

https://aliallam.app.n8n.cloud/webhook-test/start-meeting

I changed the random letters and numbers to 'start-meeting' through 'path'

### Step 2: Click "Test Workflow"

Hit the orange Test Workflow button.

You should see “Waiting for webhook call…”

If you don’t see this, the webhook won’t work, go back and fix Step 1.

### Step 3: Send Real Input using Hoppscotch

Go to https://hoppscotch.io

Set method to POST

In the URL bar, paste your test webhook URL:

https://aliallam.app.n8n.cloud/webhook-test/start-meeting

Click Body and select JSON

Paste this:

{
  "audio": "Ali is now testing the new webhook from scratch!"
}

Hit send

![image](https://github.com/user-attachments/assets/40a6b76d-e112-464f-8050-a541805eb40e)

Step 4 – Go Back to n8n and Check It Ran
The workflow should execute immediately.

Click Audio Capture and make sure your input came through correctly.

You should see:

{
  "audio": "Ali is now testing the new webhook from scratch!"
}

![image](https://github.com/user-attachments/assets/87f2b907-4235-4eae-b828-3f341df87b3e)



