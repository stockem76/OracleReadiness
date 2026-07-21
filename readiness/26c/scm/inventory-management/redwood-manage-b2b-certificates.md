[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [SCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/index.md) › [Inventory Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/scm/inventory-management.md)

# Redwood: Manage B2B Certificates

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/scm/26c/inv26c/26C-inventory-wn-f46529.htm)

You can now use a Redwood page to define, manage, and maintain the digital certificates used to enable encryption and decryption for collaboration messages exchanged with your trading partners using the AS2 protocol via Oracle B2B.

This helps protect sensitive data in transit and meet organizational security and compliance requirements.

## ⚙️ Steps to Enable and Configure

You can access this functionality by enabling the feature **Simplify Configuration and Processing for B2B Messaging**orthe profile option **ORA_CMK_MESSAGING_CERTIFICATES_REDWOOD_ENABLED.**

1. In the Setup and Maintenance work area, search for and select the **Manage Administrator Profile Values**task**.**
2. On the Manage Administrator Profile Values page, search for and select the **ORA_CMK_MESSAGING_CERTIFICATES_REDWOOD_ENABLED**profile option code.
3. In the Profile Values section, set theSite Level to **Yes**or **No**.

• Yes = enables the feature
• No = disables the feature

1. Select **Save and Close.**
2. After enabling the Redwood page, you need to log out and log in again to access the Messaging Certificates task from the task panel.

You can perform the following steps to set up digital certificates:

1. **Create Keystore Password:** Creates or sets the keystore password, which is required to securely store and access certificates and private keys in the B2B keystore.
2. **Generate Certificate:** Creates a new self-signed X.509 digital certificate and its associated key pair in the B2B keystore.
3. **Import Certificate:** Imports an external certificate or keystore into the B2B keystore so it can be used for secure messaging configuration.
4. **Generate Certificate Signing Request**: Generates a certificate signing request (CSR) using an existing key pair, which can be sent to a certificate authority (CA) to obtain a trusted, signed certificate.
5. **Export Certificate**: Exports the selected certificate from the keystore to a file (typically <alias>.cer), so it can be shared or used in B2B/AS2 configuration.
6. **Import Signed Certificate:** Imports a CA-signed certificate and associates it with the existing private key, effectively replacing the self-signed certificate for use in trusted B2B/AS2 exchanges.
7. **Delete Certificate:** Deletes the selected certificate entry (and associated private key, if present) from the B2B keystore, making it unavailable for B2B/AS2 message security.

**Create Keystore Password**

1. Navigate to **Messaging Certificates**, select **Keystore Password**.
2. Enter the password and **Save**.

Keystore Password

**Generate Certificate**

1. On the Messaging Certificates page, select **Generate**.
2. Select **Submit** after you've added the details for the new certificate.

Generate Certificate

**Import Certificate**

1. On the Messaging Certificates page, select **Import**.
2. Select **Import and Close** after you've added the details.

Import Certificate

**Generate Certificate Signing Request**

1. On the Messaging Certificates page, locate the **self-signed private key** for which you want to create a CSR.
2. In the Actions column, select **Generate Certificate Signing Request**.
3. Enter the Private Key Password for the selected key entry, then select**Save As.**
4. Choose the download location and file name. The default name is <alias>.cer.

Generate Certificate Signing Request

**Export Certificate**

1. On the Messaging Certificates page, locate the certificate to export.
2. In the Actions column, select **Export** > **Certificate**.
3. Choose the download location and file name. The default name is <alias>.cer.

Export Certificate

**Import Signed Certificate**

1. Under **Actions**, select **Import Signed Certificate.**
2. Select **Import** after you've added the details.

Import Signed Certificate

**Delete Certificate**

1. Under **Actions**, select **Delete**.
2. On a public key, select **Delete**.

Delete Public Key

1. On a private key, select **Delete** after you’ve added the required details.

Delete Private Key

## 💡 Tips and Considerations

1. Before generating or importing certificates, you must enter a keystore password.
2. The keystore password defined in Messaging Certificates needs to match the Oracle B2B keytore password.
3. Import supports two types:
• Import a certificate (.cer) file:
1. Uploads a single public certificate and stores it under the alias you provide.
2. After import, the page shows the certificate with Private Key not selected. This means it’s a public certificate only and no private key was imported.
• Import a keystore:
1. Uploads an entire keystore that may contain one or more certificates and private keys.
2. Requires the keystore password and, if applicable, a private key password so the system can read and securely store those entries.
4. The Generate option:
• Generates the public-private key pair using the selected signature algorithm and key length.
• Creates a self-signed certificate valid for the number of days specified.
• Stores it as a private key entry identified by the provided alias.
5. The Generate Certificate Signing Request prompts for the private key password to authorize use of that private key for generating the request.
6. The Export option exports the public certificate and not the private key.
7. The Import Signed Certificate updates the keystore entry, so the certificate is now Trusted (the Type changes from Self-Signed to Trusted) while continuing to use the same underlying private key.
8. The Delete option:
• Requires the private key password when deleting a certificate entry that includes a private key to confirm authorization.
• Allows deletion of a public certificate without a password since no private key material is involved.

## 🔐 Access Requirements

Users who are assigned a configured job role that contains this privilege can access this feature:

Manage B2B Certificates (CMK_MANAGE_B2B_CERTIFICATES_PRIV).

This privilege was available prior to this update.

## 📚 Key Resources

Refer to the *Configuring and Managing B2B Messaging for Oracle Fusion Cloud SCM* guide on the Oracle Help Center.

---
*Oracle Cloud Readiness · 26C · SCM · Inventory Management*