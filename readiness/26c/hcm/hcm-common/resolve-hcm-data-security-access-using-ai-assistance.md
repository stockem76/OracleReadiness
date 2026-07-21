[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [HCM Common](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/hcm-common.md)

# Resolve HCM Data Security Access using AI Assistance

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/hcom26c/26C-hcm-common-wn-f49834.htm)

The **HCM Data Security Assistant** is your AI-powered assistant designed to provide a summary of your HCM Data Security setup and resolve a user’s data security access issues quickly and accurately. It’s designed to help IT security managers troubleshoot user data access issues. This AI assistant understands the context of a user’s assigned roles, security profiles, and data access. It focuses on person-related user objects and can’t provide access details for organizations or positions.

A document tool is included so you can upload your own security documentation guidelines.

Benefits include:

• Identifying user-specific roles and privileges that grant HCM access
• Viewing security configurations
• Regenerating roles and access control lists (ACLs)
• Previewing user access; and
• Comparing security profiles between users.

**Sample Queries that the Agent can Answer**

Here are some sample queries that IT Security Managers may have when researching problems related to data security issues, which the agent can answer:

• Give an overview of my security configuration.
• Show security profiles assigned to user, TM-KLAW.
• Verify if a user can perform certain quick actions on another user.
• Roles assigned to a user.
• Security profiles associated with a role.
• Differences between roles or security profile configurations for multiple users or roles.
• Whether assignment-level data security is enabled.
• Whether Oracle Search is enabled.
• Oracle Search index status.
• How a user has access to a specific quick action.
• Whether a user has access to perform a quick action for a specific target worker.
• Regenerate or review a user’s access control list (ACL).
• Data security policies for a role.

In this example, we created an AI Agent named HCM Data Security Assistant 2601 from the preconfigured template. The IT Security Manager asks a series of questions about the current organizational and user-specific security configuration. In response to each question, the agent responds with the relevant details.

AI Assistant identifies the organization’s current data security configuration

When asking about roles and security profiles that are assigned to a specific user, you must provide their exact user name. In the examples below, one of the referenced users is TM-KLAW. Note that this person must have recently signed into Fusion Applications.

AI Assistant responds with user TM-KLAW’s assigned roles and security profiles

AI Assistant identifies how user TM-MFITZIMMONS accesses Promote Worker quick action

In this example, the Assistant identifies and shows a table-formatted comparison of the different roles between users.

AI Assistant compares assigned roles between multiple users

AI Assistant regenerates the Access Control List for a specified user

With the HCM Data Security Assistant, IT security managers have a self-service way to quickly research and troubleshoot a user’s data access details using natural-language and contextual prompts. The assistant can reduce troubleshooting time by helping verify security-related setup or regenerate a user’s ACL, so they can resume their duties sooner.

## ⚙️ Steps to Enable and Configure

• Your environment must have certain necessary configurations. Ask your help desk to contact Oracle Support, who can verify what your environment has and address any gaps. For more information, see FAQ2521 on My Oracle Cloud Support.

• Set the **Enable Security Console External Application Integration** (ORA_ASE_SAS_INTEGRATION_ENABLED) profile option to Yes and enable permission groups for the appropriate roles. See Access Requirements for AI Agent Studio.
• The HCM Data Security Assistant is a preconfigured template. You can copy it or create your own agent using the template. 
  • To learn how to set up AI agents, see Create AI Agents Using Preconfigured Agent Team Templates.

## 💡 Tips and Considerations

• A document tool is included with this agent, so that you can extend or add your own specific organizational guidelines or exceptions while training the HCM Data Security Assistant.
• When asking a user-specific data security question, you must provide the specific user name, not the person’s display name.
• Before asking the AI Agent about a specific user, ensure that user has recently signed into Fusion Applications
• This AI Assistant focuses on person-related objects; it cannot provide access details for organizations or positions, for example.
• When searching by role name, the system requires exact matches to avoid incorrect results.

## 🔐 Access Requirements

The agents you can view depend on the roles and privilege assigned to you. To access this agent, your role must be explicitly granted access to it by an AI Studio Administrator. See How can I give access to AI agents and Access Requirements for AI Agent Studio.

## 📚 Key Resources

For more information, refer to these topics on the Oracle Help Center:

• Best Practices for HCM Data Roles and Security Profiles
• Preview HCM Data Security
• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?

---
*Oracle Cloud Readiness · 26C · HCM · HCM Common*