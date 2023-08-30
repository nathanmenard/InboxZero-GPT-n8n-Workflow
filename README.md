# InboxZero-GPT-n8n-Workflow
Automate your email sorting in Gmail using GPT and n8n to achieve the coveted "Inbox Zero" status. This workflow is designed to automatically sort, label, and organize your emails to declutter your inbox efficiently.

🎬 **Watch the Tutorial**: [How to set up Inbox Zero GPT Workflow](...)

📷 **Flow Diagram**:

![Flow Diagram](https://drive.google.com/uc?export=view&id=1zH93sR707oF5HenGJrprXtinmLfsyrjI)

---

# Installation Guide


## Step-by-Step Setup

### 1. Get GPT API Key
- Go to [OpenAI's signup page](https://platform.openai.com).
- Complete the signup process and obtain your GPT API key.
- Save this API key, as you'll need it to configure the n8n workflow.

### 2. Get Gmail OAuth for n8n
- Visit the [Google Developer Console](https://console.developers.google.com/).
- Create a new project and navigate to "Credentials".
- Enable the Gmail API and configure OAuth consent screen.
- Download the JSON file which includes your OAuth 2.0 Client IDs and Client Secret.
- Store these credentials safely for later use in n8n.

### 3. Create n8n Account
- Sign up for an n8n account [here](https://n8n.io/?ref=nzyxngm&utm_source=affiliate).
- Once registered, install the n8n software according to their documentation.

### 4. Initial n8n Setup
- Open n8n and initiate a new workflow.
- Replace placeholder values in the first set of nodes with your GPT API key and Gmail OAuth credentials.

### 5. Activate Shortcuts for Inbox Zero (Azerty French Version)
- In Gmail settings, go to "See all settings".
- Go to "Keyboard shortcuts" and configure them as follows (French AZERTY layout):
    - Archive: `e`
    - Answer all: `a`
    - Answer: `r`
    - Label: `l`
    - Navigate Emails: `j` and `k`

### 6. Get Gmail Label IDs for n8n
- In Gmail, right-click on a label and select "Label color" then "Label code".
- Copy the label IDs for each label you want to use.
- Add these IDs to the respective Gmail nodes in your n8n workflow.

### 7. Gmail Inbox Setup
- Create or rename labels in Gmail as follows:
    1. `noActionNeeded`
    2. `interestingNews`
    3. `importantInfo`
    4. `needsResponse`
- Update the Gmail nodes in n8n to use these label IDs for sorting.

### 8. Testing the Workflow
- In the Gmail node titled "Gmail_GetEmailOverviews" in n8n, set the limit to 5-10 emails.
- Run the workflow in n8n to ensure it sorts and labels emails as expected.

### 9. Run it Full
- Once testing is successful, remove or adjust the email limit in "Gmail_GetEmailOverviews".
- Execute the workflow to sort your full inbox.

---

# Usage
After setting up the workflow, any new or existing email in your Gmail inbox will automatically be sorted and labeled according to the rules you've defined.

For more information and troubleshooting, refer to the [tutorial video](...).

---

Feel free to fork, star, and contribute to this repository.

Enjoy your organized inbox! 💌
