[📋 26C](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/index.md) › [HCM](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/index.md) › [Learning and Development](https://github.com/stockem76/OracleReadiness/blob/main/readiness/26c/hcm/learning-and-development.md)

# Redwood Media Player Updates

`⚙️ Steps to Enable` · `💡 Tips & Considerations`

> 📖 [View on Oracle Help Center](https://docs.oracle.com/en/cloud/saas/readiness/hcm/26c/lear-26c/26C-learning-wn-f49569.htm)

The Redwood media player is now the default experience in new implementations for video-based learning content.

This update:

• Fixes Chrome audio issues
• Disables Picture-in-Picture for learning videos
• Hides play, pause, fast-forward, and rewind controls when a trailer plays on a Learning Catalog card
• Plays videos unmuted by default
• Shows duration correctly
• Follows learning fast-forward rules

Improve consistency and reliability across video-based learning experiences while supporting more standardized playback behavior across implementations.

## ⚙️ Steps to Enable and Configure

This player is now enabled by default for all new implementations.

If you have an existing implementation, set the site-level profile value to Yes for the ORA_WLF_SP_MEDIA_PLAYER profile option. Go to Setup and Maintenance > Tasks panel > Search > Manage Administrator Profile Values.

## 💡 Tips and Considerations

JW Player support is limited, so customers with existing implementations should move to the Redwood media player.

---
*Oracle Cloud Readiness · 26C · HCM · Learning and Development*