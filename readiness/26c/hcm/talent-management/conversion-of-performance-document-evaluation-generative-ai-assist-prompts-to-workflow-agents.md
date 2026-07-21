[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# Conversion of Performance Document Evaluation Generative AI Assist Prompts to Workflow Agents

`⚙️ Steps to Enable` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f50136.htm)

Leverage these Performance Management workflow agents in AI Agent Studio for AI Assist generated evaluation content in performance documents and All-in-One Evaluations. These agents replace the earlier Generative AI prompts used for creating the performance document comments.

• **Agent Teams**
• **Performance Evaluation Manager Overall Summary Generator** - Generates evaluation comments for a manager on an overall summary in a performance document
• **Performance Evaluation Manager Performance Goal Generator** - Generates evaluation comments for a manager on performance goal items and summary in a performance document
• **Performance Evaluation Manager Development Goal Generator -**Generates evaluation comments for a manager on development goal items and summary in a performance document
• **Performance Evaluation Manager Competency Generator** - Generates evaluation comments for a manager on competency items and summary in a performance document
• **Performance Evaluation Manager Dynamic Skill Generator** - Generates evaluation comments for a manager on dynamic skill items and summary in a performance document
• **Performance Evaluation Employee Overall Summary Generator** - Generates evaluation comments for a employee on an overall summary in a performance document
• **Performance Evaluation Employee Performance Goal Generator** - Generates evaluation comments for a employee on performance goal items and summary in a performance document
• **Performance Evaluation Employee Development Goal Generator** - Generates evaluation comments for a employee on development goal items and summary in a performance document
• **Performance Evaluation Employee Competency Generator** - Generates evaluation comments for an employee on competency items and summary in a performance document
• **Performance Evaluation Employee Dynamic Skill Generator** - Generates evaluation comments for a employee on dynamic skill items and summary in a performance document
• **Performance Evaluation Matrix Manager Overall Summary Generator** - Generates evaluation comments for a matrix manager on an overall summary in a performance document.
• **Performance Evaluation Matrix Manager Performance Goal Generator** - Generates evaluation comments for a matrix manager on performance goal items and summary in a performance document
• **Performance Evaluation Matrix Manager Development Goal Generator** - Generates evaluation comments for a matrix manager on development goal items and summary in a performance document
• **Performance Evaluation Matrix Manager Competency Generator** - Generates evaluation comments for a matrix manager on competency items and summary in a performance document
• **Performance Evaluation Matrix Manager Dynamic Skill Generator** - Generates evaluation comments for a matrix manager on dynamic skill items and summary in a performance document
• **Performance Evaluation Participant Overall Summary Generator** - Generates evaluation comments for a participant on an overall summary in a performance document
• **Performance Evaluation Participant Performance Goal Generator** - Generates evaluation comments for a participant on performance goal items and summary in a performance document
• **Performance Evaluation Participant Development Goal Generator**- Generates evaluation comments for a participant on development goal items and summary in a performance document
• **Performance Evaluation Participant Competency Generator** - Generates evaluation comments for a participant on competency items and summary
• **Performance Evaluation Participant Dynamic Skill Generator** - Generates evaluation comments for a participant on dynamic skill items and summary in a performance document.
• **Performance Document Check-in Summary Generator** - Generates a summary of an employee's check-ins to display in a performance document.

• **Agents**
• **Performance Evaluation Participant Feedback Summary Generator** - Generates a summary of an employee's participant feedback in a performance document to use for evaluation comments
• **Performance Evaluation Interim Feedback Summary Generator** - Generates a summary of an employee's interim feedback to use for evaluation comments in a performance document
• **Performance Evaluation Anytime Feedback Summary Generator** - Generates a summary of an employee's anytime feedback to use for evaluation comments in a performance document
• **Performance Evaluation Requested Feedback Summary Generator** - Generates a summary of an employee's requested feedback to use for evaluation comments in a performance document
• **Performance Evaluation Employee Check-In Summary Generator**- Generates a summary of an employee's check-in discussion notes and questionnaire responses to use for evaluation comments in a performance document
• **Performance Evaluation Manager Check-In Summary Generator** - Generates a summary of a manager's check-in discussion notes and questionnaire responses to use for evaluation comments in a performance document.

**Note:**The transition to the new agents is required and will happen automatically as part of this release, so no opt-in or manual action is needed. However, you can’t use the AI Configurator tool from now on to modify the generative AI prompts and will need to recreate the prompt customizations that were done for the generative AI prompts in the workflow agents.

Use these workflow agents to support evaluation generating experiences such as:

• Summarizing participant feedback, interim feedback, anytime feedback, requested feedback and check-in summaries to be used in the evaluation comment generating prompts.
• Generating evaluation comments for managers, employees, regular participants and matrix manager participants across: 
  • Section summaries
• Performance goals
• Development goals
• Competencies
• Dynamic Skills
• Questionnaires

## ⚙️ Steps to Enable and Configure

**Note**:  The switch to the new agents is automatic and can't be skipped.

Your environment must have certain necessary configurations. Ask your help desk to contact Oracle Support, who can verify what your environment has and address any gaps. For more information, see FAQ2521 on My Oracle Cloud Support.

Set these profile option values as indicated in the table.

Profile Option Name | Profile Option Code | Value
Enable Security Console External Application Integration | ORA_ASE_SAS_INTEGRATION_ ENABLED | Yes
Enable VBCS Progressive Web Application User Interface | ORA_HCM_VBCS_PWA_ENABLED | Y

For more information about setting profile option values, see How do I enable a profile option?.

Enable permission groups for appropriate roles. For more information, see Access Requirements for AI Agent Studio.

To learn how to set up AI workflow agents, see Create AI Agents Using Preconfigured Agent Team Templates.

## 🔐 Access Requirements

The agents you can view depend on the roles and privileges assigned to you. To access an agent, your role must be explicitly granted access to it by an AI Studio Administrator. For more information, see How can I give users access to AI agents and Access Requirements for AI Agent Studio.

## 📚 Key Resources

• Explore AI Agents for Oracle Fusion Cloud Applications
• How do I use AI Agent Studio?
• Deprecation of AI Configurator and Transition to AI Agent Studio

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*