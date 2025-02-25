# Setting Up Google Email with SMTP

This guide walks you through setting up a Google email account with SMTP for use in your application's email functionality.

## Prerequisites

- A Google account
- Two-factor authentication enabled on your Google account

## Step 1: Set Up a Passkey and Enable 2-Factor Authentication

### Creating a Passkey

1. Go to your [Google Account: https://myaccount.google.com/](https://myaccount.google.com/). If you don't have one yet, create one.
2. Select **Security** from the left navigation panel
3. Under "Signing in to Google," select **Passkeys**
4. Click **Create a passkey**
5. Follow the on-screen instructions:
   - You may need to verify your identity
   - Choose the device you want to use for your passkey (your current device is usually the default)
   - Complete the verification process (fingerprint, face scan, or PIN, depending on your device)
6. Confirm the creation of your passkey

### Enable 2-Factor Authentication

1. Go back to the **Security** section of your Google Account
2. Under "Signing in to Google," select **2-Step Verification**
3. Click **Get Started**
4. Verify your identity if prompted
5. Follow the on-screen instructions to set up your preferred 2FA method (phone, authenticator app, etc.)
6. Complete the verification and confirm enabling 2FA

## Step 2: Generate an App Password

Once 2FA is enabled, you'll need to generate an app password for your application to use:

1. Go to [App Passwords: https://myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords)
   - Note: This page is only accessible if you have 2FA enabled
2. Select **App** from the dropdown menu and choose "Other (Custom name)"
3. Enter a name for your application (e.g., "My App")
4. Click **Generate**
5. Google will display a 16-character password - save this password as you'll need it for your configuration
6. Click **Done**

## Step 3: Configure Your Application

Navigate to your SYSTEM_FOLDER/src/ and update your `config.development.php` file with the following SMTP settings:

```php
"SMTP" => [
    "PHPMAILER_MAILER" => "smtp", // PHPMailer mailer
    "SERVER" => "smtp.gmail.com", // SMTP server
    "SERVER_PORT" => 587, // SMTP server port
    "SECURE_OPTION" => "tls",
    "SERVER_USERNAME" => "your.email@gmail.com", // Your Gmail address
    "SERVER_PASSWORD" => "your-16-character-app-password-without-spaces", // The app password generated in Step 2 (space removed)
],
"SENDER_EMAIL" => "no-reply@your-domain", // The sender email that will appear to recipients
```

Replace:
- `your.email@gmail.com` with your actual Gmail address
- `our-16-character-app-password-without-spaces` with the app password you generated

## Important Notes

- The app password is a 16-character code that gives your application permission to access your Google Account
- App passwords are less secure than your main password, so use them only for applications you trust
- You can revoke app passwords at any time from your Google Account security settings
- The `SENDER_EMAIL` field can be different from your actual Gmail address, but emails will still be sent through your Gmail account

## Troubleshooting

If you encounter issues:

1. Ensure 2FA is properly enabled on your account
2. Verify that you've correctly copied the 16-character app password
3. Make sure your Gmail account hasn't been blocked for security reasons
4. Check if "Less secure app access" is required for your account type

## Security Considerations

- Never share your app password
- Regularly review and revoke unused app passwords
- Consider using environment variables for storing sensitive information like passwords
