[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Learning and Development](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/learning-and-development.md)

# My Learning training hours

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/lear-26c/26C-learning-wn-f49624.htm)

Your learning experiences now include a scoreboard that helps you track learning progress over time. See training hours, enrollments, required learning, and learning still to complete for the current and previous year. Show and hide relevant cards so that the scoreboard best supports your needs.

My Learning Experiences Page Showing the New Scoreboard

Increase visibility into learning progress by presenting total training hours and enrollment counts for current and previous years in a clear, consistent scoreboard. Simplify tracking with static values unaffected by filters, ensuring reliable year-based metrics. Improve decision-making by supporting training hours calculated from actual or expected effort, reflecting accurate learner engagement.

## ⚙️ Steps to Enable and Configure

This feature requires manual configuration in Visual Builder Express to enable and customize the scoreboard display.

• Use the learningMonth page property to set the first month of the learning year for the scoreboard metrics.
• Use the propertyeffortValue page property to set the type of effort for yearly scoreboard calculations to use: expected effort or actual effort
• Use the myLearningExperiencesScoreCards page property to specify whether the scoreboard appears on the the page and the order of the scorecards.

## 💡 Tips and Considerations

• Scoreboard values for training hours and enrollment counts remain static and don't update based on search or filter selections.
• Training hours are calculated using either actual effort or expected effort, based on configuration and include only assignments with complete or bypass completed status. Partial completions aren't counted.
• Learning path assignments contribute to training hours only when their status is bypass completed.
• Expected effort calculation uses the maximum value when both minimum and maximum are defined for courses and learning paths.

---
*Oracle Cloud Readiness · 26C · HCM · Learning and Development*