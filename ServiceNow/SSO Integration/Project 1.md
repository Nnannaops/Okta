# Okta and ServiceNow SSO Integration

## Overview
This project demonstrates how to configure Single Sign-On (SSO) between **Okta** and **ServiceNow**. The goal is to enable seamless access for users from Okta to ServiceNow, enhancing security and simplifying the login process.

## Prerequisites
- **Okta Account** with admin access
- **ServiceNow Instance** with admin privileges
- Knowledge of SAML 2.0 or other SSO protocols

## Project Structure
- **Screenshots** folder: Contains all relevant screenshots of configurations and results
- **Configuration Files** (if any): Placeholder for configuration exports or code snippets

## Setup Steps

### 1. Configuring Okta for SSO
1. Log in to **Okta** and navigate to **Applications**.
2. Click on **Add Application** and search for **ServiceNow**.
3. Configure SAML settings as follows:
   - **Single Sign-On URL**: `<ServiceNow_SSO_URL>`
   - **Audience URI (SP Entity ID)**: `<ServiceNow_Entity_ID>`
4. Complete the setup and assign users.

### 2. Setting up ServiceNow to Accept Okta SSO
1. Log in to your **ServiceNow** instance.
2. Go to **Multi-Provider SSO** > **Identity Providers**.
3. Add **Okta** as a new identity provider using SAML 2.0.
   - **Identity Provider's SingleLogoutRequest**: `<Okta_SLO_URL>`
   - **NameID format**: `<Format_Type>`
4. Save the configuration and test the connection.

### 3. Testing the SSO Configuration
1. Log out of **ServiceNow**.
2. Log in through **Okta** and verify access to ServiceNow.
3. Check for any errors in the SSO logs.

## Screenshots
| Step | Description | Screenshot |
|------|-------------|------------|
| Okta SSO Setup | Configuring Okta for ServiceNow | ![Okta Setup](./screenshots/okta-setup.png) |
| ServiceNow Config | Adding Okta as an Identity Provider | ![ServiceNow Config](./screenshots/servicenow-config.png) |
| Testing | Successful SSO Login | ![Testing SSO](./screenshots/testing-sso.png) |

## Troubleshooting
- **Common Errors**: Tips for resolving configuration mismatches, certificate issues, etc.
- **Okta Logs**: How to access and interpret logs in Okta for troubleshooting.

## Additional Resources
- [Okta Documentation](https://developer.okta.com/docs/)
- [ServiceNow Documentation](https://docs.servicenow.com/)

## Author
[Nnanna Nwoke](https://www.linkedin.com/in/your-profile)
