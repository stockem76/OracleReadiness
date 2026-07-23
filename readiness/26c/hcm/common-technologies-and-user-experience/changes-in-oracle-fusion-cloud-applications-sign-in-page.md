[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Common Technologies and User Experience](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/common-technologies-and-user-experience.md)

# Changes in Oracle Fusion Cloud Applications Sign In page

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/common/26c/common26c/26C-common-wn-f49504.htm)

Identity and access management for Fusion Applications will be upgraded to Oracle Cloud Infrastructure (OCI) Identity and Access Management if your existing environments aren't already on it. The identity upgrade for your environment family will be scheduled separately, not in the same month as a quarterly update. New environment families and environments created after April 6, 2025 are already on OCI Identity and Access Management, so they don't need an upgrade.

For environments on OCI Identity and Access Management, the Fusion Applications Sign In page looks different from the Sign In page for environments not on OCI Identity and Access Management.

This is what the Sign In page looks like to users, depending on the scenario with their environment and whether they’re on federated Single Sign-On (SSO) or not.

Scenario with the Environment | Federated SSO | Non-Federated SSO
Not on OCI Identity and Access Management |  | 
On OCI Identity and Access Management |  |

The changes to the Sign In page are a result of environments being on OCI Identity and Access Management, and these changes also provide an improved experience for the users.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• After the identity and access management upgrade, some users might be asked to change their password when they try to sign in.
• Even though environment families and environments created after April 6, 2025 may be on OCI Identity and Access Management by default, there might be a lag before that actually happens.

---
*Oracle Cloud Readiness · 26C · HCM · Common Technologies and User Experience*