[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Learning and Development](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/learning-and-development.md)

# Summary and Description Generator Updates

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/lear-26c/26C-learning-wn-f49656.htm)

Existing AI-assisted summary and description generation now uses workflow automation agents. These agents support learning summaries and descriptions, bulk learning descriptions, and generic text summaries used in Learning Catalog advisor search. And they continue to support the same application-page and process flows where AI-assisted generation is already available.

Preserve existing AI-assisted authoring and recommendation experiences while moving them to secured workflow agents. Reduce regression risk across learning flows and keep summary and description generation available for learning specialists, employees, and managers.

## ⚙️ Steps to Enable and Configure

Grant the appropriate duty roles. See Access Requirements for details.

## 💡 Tips and Considerations

• Some workflow agents are invoked directly from application pages, while process-only agents run in the background and are not selected by users.
• The migrated workflow agents work in the same application pages and processes where AI-assisted generation is already available.

## 🔐 Access Requirements

Learning specialists working with these workflow automation agents need these duty roles. Make sure to add them to your applicable custom roles.

Agent Name and Code | Duty Role That Secures It | Role Granted or To Be Granted | Use in Applicable Flow
Bulk Learning Descriptions Assistant ORA_HCM_WLF_BULK_LEARN_DESC_ASSIST | Learning and Development Agents Duty ORA_DR_WLF_LEARN_DEV_AGENTS_DUTY | Learning Specialist | Creates multiple learning descriptions based on learning titles and any existing description text.
Learning Description Assistant ORA_HCM_WLF_LEARN_DESC_ASSISTANT | Learning and Development Agents Duty ORA_DR_WLF_LEARN_DEV_AGENTS_DUTY | Learning Specialist | Creates a learning item description from the title and any existing description text.
Learning Summary Assistant ORA_HCM_WLF_LEARN_SUMMARY_ASSISTANT | Learning and Development Agents Duty ORA_DR_WLF_LEARN_DEV_AGENTS_DUTY | Learning Specialist | Creates a learning item summary from the title, description, and any existing summary text.
GenAI Completion hcm.wlf.gen_ai_completion | Generic Text Summary Assistant Duty ORA_DR_WLF_GENERIC_TEXT_SUMMARY_ASSISTANT_DUTY | Employee and Line Manager | Supports generic text summary use cases, including Learning Catalog advisor search and learning suggestions from employee or manager check-in feedback.

---
*Oracle Cloud Readiness · 26C · HCM · Learning and Development*