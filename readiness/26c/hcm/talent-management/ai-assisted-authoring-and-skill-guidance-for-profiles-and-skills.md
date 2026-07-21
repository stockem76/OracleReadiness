[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Talent Management](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/talent-management.md)

# AI-Assisted Authoring and Skill Guidance for Profiles and Skills

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/tama-26c/26C-talent-mgmt-wn-f49848.htm)

Existing AI-assisted summary and description generation, as well as ESS jobs that require summarization services across profiles and skills, now use workflow automation agents. These agents support skill descriptions, capability guide descriptions, job profile and position profile authoring assistance, skill rating assessment advisors for specialists, skill rating advisors for employees, and ESS jobs that summarize jobs, skills, and organization information. They continue to support the same application pages and process flows where AI-assisted generation is already available.

Preserve existing AI-assisted authoring, summarization, and recommendation experiences while moving them to secured workflow agents. Reduce regression risk for profile and skills flows and ESS jobs, and keep AI-assisted authoring, summary generation, and description generation available for learning specialists and employees.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• Some workflow agents are invoked directly from application pages, while process-only agents run in the background and are not selected by users.
• The migrated workflow agents work in the same application pages and processes where AI-assisted generation is already available.

## 🔐 Access Requirements

The agents you can view depend on the roles and privileges assigned to you. To access the Grow Coach agent, your role must be explicitly granted access to it by an AI Studio Administrator. See How can I give users access to AI agents and Access Requirements for AI Agent Studio.

Human resources specialists and employees working with these workflow automation agents need these duty roles. Make sure to add them to your applicable job roles.

Agent Name and Code | Duty Role that Secures it | Seeded Role Granted to or Must be Granted to | Use in Application Flow
Capability Guide Description Assistant ORA_HCM_WLF_CAPABILITYGUIDE_DESC_ASSISTANT | Learning and Development Agents Duty ORA_DR_WLF_LEARN_DEV_AGENTS_DUTY | Learning Specialist job role | Creates capability guide descriptions from the role guide, capability guide name, and available descriptions.
Skill Description Assistant ORA_HCM_HRT_SKILL_DESC_ASSISTANT | Profiles and Skills Library Agents Duty ORA_DR_HRT_PROFILES_SKILLS_LIBRARY_AGENTS_DUTY | Human Resource Specialist job role | Creates skill descriptions from skill name, draft description, business need, domain, and business function.
Job Profile Authoring Assistant ORA_HCM_HRT_JOB_PROFILE_AUTH_ASSISTANT | Profiles and Skills Library Agents Duty ORA_DR_HRT_PROFILES_SKILLS_LIBRARY_AGENTS_DUTY | Human Resource Specialist job role | Generates job profile content, including summaries, descriptions, responsibilities, and qualifications.
Position Profile Authoring Assistant ORA_HCM_HRT_POSITION_PROFILE_AUTH_ASSISTANT | Profiles and Skills Library Agents Duty ORA_DR_HRT_PROFILES_SKILLS_LIBRARY_AGENTS_DUTY | Human Resource Specialist job role | Generates position profile content, including summaries, descriptions, responsibilities, and qualifications.
Skills Rating Advisor ORA_HCM_HRT_SKILLS_RATING_ADVISOR | Profiles and Skills Library Agents Duty ORA_DR_HRT_PROFILES_SKILLS_LIBRARY_AGENTS_DUTY | Human Resource Specialist job role | Generates skill rating assessments that help employees select an appropriate skill level rating.
Organization Summarizer hcm.wlf.organization_summarizer | Profiles and Skills Library Agents Duty ORA_DR_HRT_PROFILES_SKILLS_LIBRARY_AGENTS_DUTY | Human Resource Specialist job role | ESS job Create Summaries using Generative AI creates organization summaries when Organization is selected.
Job Summarizer hcm.wlf.job_summary_synthesizer | Profiles and Skills Library Agents Duty ORA_DR_HRT_PROFILES_SKILLS_LIBRARY_AGENTS_DUTY | Human Resource Specialist job role | ESS job Create Summaries using Generative AI creates job summaries when Jobs is selected.
Skill Summarizer hcm.wlf.skill_summary_synthesizer | Profiles and Skills Library Agents Duty ORA_DR_HRT_PROFILES_SKILLS_LIBRARY_AGENTS_DUTY | Human Resource Specialist job role | ESS job Create Summaries using Generative AI creates skill summaries when Skills is selected.
Next Best Jobs hcm.wlf.next_best_jobs | Profiles and Skills Library Agents Duty ORA_DR_HRT_PROFILES_SKILLS_LIBRARY_AGENTS_DUTY | Human Resource Specialist job role | Recommendation Profile generates next-best career role recommendations that appear in Opportunity Marketplace recommendations and Grow career role recommendations.

---
*Oracle Cloud Readiness · 26C · HCM · Talent Management*