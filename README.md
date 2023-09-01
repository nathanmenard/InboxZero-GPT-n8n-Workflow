# InboxZero-GPT-n8n-Workflow
Automate your Gmail inbox with GPT and n8n. This workflow sorts, labels, and organizes your emails for a streamlined "Inbox Zero" experience.

🎬 **Tutorial Video**: [Inbox Zero GPT Workflow Setup](...)

📷 **Flow Diagram**:  
![Flow Diagram](https://drive.google.com/uc?export=view&id=1sWfQE_f8TPOUE2m7voGMtDKmZ2EunE49)

---

# Installation Guide

## Step-by-Step Instructions

### 1. Set Up n8n
- [Register for an n8n account](https://n8n.io/?ref=nzyxngm&utm_source=affiliate).
- Download `GPT_Gmail_AutoSort_for_Inbox_Zero.json` from this repository.
- In n8n, click "Import from File..." in the top-right and upload the JSON file.
- In the `SetUserProfileData` node, configure all fields except the label fields.

### 2. Obtain GPT API Key
- [Register at OpenAI](https://platform.openai.com) and get your GPT API key.
- Insert the API key into the workflow's GPT node.

### 3. Configure Gmail OAuth in n8n
- In n8n, click a Gmail node, add an account, and copy the "OAuth Redirect URL."
- Go to [Google Developer Console](https://console.developers.google.com/).
- Create a new project, go to "Credentials," enable Gmail API, and configure the OAuth consent screen.
- Download the JSON file containing your OAuth 2.0 Client IDs and Secret.

### 4. Set Gmail Shortcuts (Azerty French Version)
- Open Gmail settings and navigate to "See all settings."
- Enable "Keyboard shortcuts" if they are not activated.
- Configure keyboard shortcuts as follows for the French AZERTY layout:
  - Archive: `e`
  - Reply All: `a`
  - Reply: `r`
  - Label: `l`
  - Navigate: `j` and `k`

### 6. Create Gmail Labels
- Rename or create Gmail labels as follows:
  1. `n8nNoActionNeeded`
  2. `n8nInterestingNews`
  3. `n8nImportantInfo`
  4. `n8nNeedsResponse`
  5. `n8nError`

### 5. Fetch Gmail Label IDs
- In n8n, create a new Gmail node with the "Get many labels" action.
- Select the 5 label IDs that correspond to the labels you created.
- Insert these IDs into the `SetUserProfileData` node and then remove the Gmail node you created.

### 6. Set Up Multiple Inboxes in Gmail
- In Gmail settings, go to the "Inbox" tab.
- Enable "Multiple Inboxes" and set up the sections using label queries like "l:n8nError in:inbox."

### 7. Test the Workflow
- In the Gmail node titled "Gmail_GetEmailOverviews" in n8n, set the email limit to 5-10.
- Run the workflow to check that it sorts and labels emails properly.

### 8. Go Live
- Once the testing is satisfactory, remove or adjust the email limit.
- Execute the workflow to organize your full inbox.

---

# How to Use
After setup, your Gmail inbox will automatically sort and label new and existing emails.

For troubleshooting and more, refer to the [tutorial video](...).

---

Feel free to fork, star, and contribute to this repository. Enjoy a cleaner inbox! 💌
