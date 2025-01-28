# Zoho CRM Integration Script

This script provides functions to integrate with Zoho CRM. It includes the following functionalities:
- Generating refresh tokens
- Generating access tokens
- Retrieving records from Zoho CRM
- Inserting leads into Zoho CRM
- Attaching files to leads

## Prerequisites

1. A Zoho CRM account with API access enabled.
2. A valid **Client ID**, **Client Secret**, **Redirect URL**, and **Zoho Code** obtained from Zoho's API console.
3. PHP installed on your server with the following extensions enabled:
   - `cURL`
   - `JSON`

## Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/zoho-crm-integration.git
Navigate to the directory:
bash
Copy
Edit
cd zoho-crm-integration
Update the constants in the script with your Zoho credentials:
php
Copy
Edit
define("ClientID", "Your Zoho Client ID");
define("ClientSecret", "Your Zoho Client Secret");
define("RedirectUrl", "Your Redirect URL");
define("ZohoCode", "Your Zoho Code");
define("RefreshToken", "Your Zoho Refresh Token");
Functions
1. generate_refresh_token()
Generates a refresh token required for long-term API access.

2. generate_access_token()
Generates an access token using the refresh token. The access token is required for making API requests.

3. get_records()
Fetches records from the Leads module in Zoho CRM.

4. insert_leads()
Adds a new lead to Zoho CRM with predefined attributes.

5. attachment_data($lead_id, $filePaths)
Uploads files to Zoho CRM and associates them with a lead.

6. create_all_lead()
Combines the insertion of leads and attachment of files into one function.

7. dump_and_die($data)
Utility function to debug data by printing and halting execution.

Usage
Generate a Refresh Token
php
Copy
Edit
generate_refresh_token();
Create a New Lead and Attach Files
php
Copy
Edit
create_all_lead();
Fetch Records
php
Copy
Edit
get_records();
Customize Lead Data
You can modify the data array inside insert_leads() to include the desired fields and values.

Notes
Replace the placeholders in the constants with actual values from Zoho.
Ensure your redirect URL matches the one registered in Zoho's API console.
Update the file paths in attachment_data with the actual paths to your files.
Logging and Debugging
API responses are logged via echo statements in the script.
Use dump_and_die() to debug specific responses during development.
