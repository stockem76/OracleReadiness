[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Learning and Development](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/learning-and-development.md)

# Self-paced learning content knowledge indexing

`⚙️ Steps to Enable` · `💡 Tips & Considerations` · `🔐 Access Requirements`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/lear-26c/26C-learning-wn-f49629.htm)

You can now turn on the **Extract the knowledge in this content for AI agents to use** checkbox for supported content types, including these types:

• Document (PDF)
• Video (MP4)
• Presentation (PPS, PPT, PPSX, PPTX)
• Online content (SCORM 1.2, SCORM 2004, AICC, CMI5)

Indexed knowledge from this content can support AI agents, such as My Tutor and Catalog Search Advisor. My Tutor can use the indexed knowledge during teaching, and Catalog Search Advisor can use the content itself in search results.

New Learning Page with the New Checkbox Selected

Improve AI response quality by making approved learning content reusable by AI agents. Support richer knowledge use across learning content and search experiences.

## ⚙️ Steps to Enable and Configure

You don't need to do anything to enable this feature.

## 💡 Tips and Considerations

• The Extract the knowledge in this content for AI agents to use checkbox can be hidden, made read-only, or given a default value using the learningItemNeedsKnowledgeIndexing attribute in Visual Builder Studio business rules.
• When source content changes, indexing updates accordingly, including cleanup and re-index scenarios.
• Disabling extraction removes indexed knowledge for that content.
• Re-enabling extraction indexes the latest available version.

## 🔐 Access Requirements

Learning specialists who create or edit self-paced learning needs these Spectra Authorization Service duty roles to invoke the AI agents indexing the knowledge. Add them to your application job roles.

Role Name | Code | Description
Learning Knowledge Index Generator | ORA_DR_WLF_LEARNING_KNOWLEDGE_INDEX_GENERATOR_DUTY | Grants access to the Learning Knowledge Index Generator agents.

## 📚 Key Resources

How do I use AI Agent Studio?

---
*Oracle Cloud Readiness · 26C · HCM · Learning and Development*