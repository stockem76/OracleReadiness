[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Common Technologies and User Experience](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/common-technologies-and-user-experience.md)

# Multifactor Authentication (MFA)

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/common/26c/common26c/26C-common-wn-f49620.htm)

If you’re creating a new environment family from 25D onwards, the environments are on Oracle Cloud Infrastructure (OCI) Identity and Access Management, and your users must enroll in multifactor authentication (MFA) for signing in to Oracle Fusion Cloud Applications. Users will be prompted to enroll for the available MFA options, as soon as they try to sign in. The only exception is that users logging in through corporate Single Sign-On (SSO) credentials won't be prompted to enroll.

New environment families and environments created after April 6, 2025 and before 25D are also on OCl Identity and Access Management. But users can optionally set up MFA when they sign in to a non-federated single sign-on (SSO) environment.

For existing environments that aren't already on OCI Identity and Access Management, the identity and access management for Fusion Applications will be upgraded to it. The identity upgrade for your environment family will be scheduled separately, not in the same month as a quarterly update. After the identity upgrade, users can optionally set up MFA when they sign in to a non-federated single sign-on (SSO) environment.

**Enable Secure Authentication**

Users can or must enable secure authentication when they sign in. MFA enrollment is mandatory for users in new environment families, but optional for existing environment families.

1. Sign in to the application using your application user ID and password. If mandatory MFA applies to you, skip to step 5.
2. Click your user image or name in the global header, and on the **Settings and Actions** menu, select **Set Preferences**.
3. On the General Preferences section, click **Password**.
4. On the General Preferences: Reset Password page, click **Manage Secure Verification**.

   You’re directed to the Oracle Cloud Console.
5. Select a method and complete the verification.

     
  
Select Secure Authentication Method
• If you select **Mobile App**, you have two modes to choose from. 
    • Follow the steps under **Configure Authenticator App** to set up push-based Oracle Mobile Authenticator App.
• Select **Use Offline Mode or another Authenticator App** to set up offline Oracle Mobile Authenticator App. You can then enter the passcode.
• If you select **Phone Number**, a one-time passcode is sent to that number. Enter the passcode and verify your phone number.
• If you select **Email**, a one-time passcode is sent to your email address. Enter the passcode and verify your email address.
• If you select **Passkey**, you can click **Configure** and save a passkey from the available options.
6. After you successfully enroll a factor, you can continue to configure additional secure verification methods.

After you’ve set up MFA, you use it as a second factor of authentication for signing in. To make further changes to your MFA setup, you can use the **Manage Secure Verification** link on the General Preferences: Reset Password page.

Here are the business benefits of enabling MFA in your environment:

• Enhanced security with multiple layers of authentication
• Reduced risk of unauthorized access and data breaches
• Facilitation of secure remote access for distributed teams

## ⚙️ Steps to Enable and Configure

You don't have to do anything to enable this feature.

**Optionally Determine the MFA Factors Available to Users**

For environments on OCI Identity and Access Management, security administrators can select which authentication options are available to users by managing user categories in the Security Console.

1. On the User Categories page of Security Console, select a user category.
2. Click **Two-Factor Authentication**.
3. Click **Edit**.
4. Select the authentication options that you want for your users. All are available to them by default. 
  • Email
• SMS
• Oracle Mobile Authenticator Passcode
• Oracle Mobile Authenticator Notification
• Fast ID Online (FIDO) Passkey Authenticator
• Bypass code
5. Click **Save and Close**.

## 💡 Tips and Considerations

• This feature is not applicable for end users logging in through Corporate Single Sign-On (SSO) credentials.
• Even though environment families and environments created after April 6, 2025 may be on OCI Identity and Access Management by default, there might be a lag before that actually happens.

## 🔐 Access Requirements

To manage the MFA settings in Security Console, administrators must be assigned the IT Security Manager role.

---
*Oracle Cloud Readiness · 26C · HCM · Common Technologies and User Experience*