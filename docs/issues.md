---
title: Known issues
summary:
authors:
    - Aaron Parker
---
## Microsoft Teams

Microsoft Teams defaults defined in [`desktop-config.json`](https://github.com/aaronparker/image-customise/blob/main/src/desktop-config.json) don't take effect as intended.

The intention is to configure Teams before first sign-in, including preventing automatic launch and setting application language. Teams will launch on first sign-in; however it will not launch automatically on subsequent sign-ins.

![Microsoft Teams application settings](assets/img/teams-application.png)

Additionally, the language still defaults to English (United States).

![Microsoft Teams language settings](assets/img/teams-language.png)

This configuration is currently disabled, but you can reinstate by updating `User.Client.json` - move the `desktop-config.json` into the `Copy` section:

```json
    "Files": {
        "Copy": [],
        "OtherFiles": [
            {
                "Source": "desktop-config.json",
                "Destination": "C:\\Users\\Default\\AppData\\Roaming\\Microsoft\\Teams\\desktop-config.json"
            }
        ]
    }
```
