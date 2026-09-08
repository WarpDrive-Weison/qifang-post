# Evidence model

Use the strongest independently observed state and keep lower states distinct.

| State | Minimum evidence | Do not claim |
| --- | --- | --- |
| `PREPARED` | Local video and intended metadata are loaded in 齐放Post | Platform upload started |
| `UPLOADING` | Platform accepted the file and transport is active | A trustworthy percentage when none is exposed |
| `UPLOADED` | Platform reports transport complete | Form complete or submitted |
| `FORM_READY` | Video and every required fingerprinted field read back correctly | Permission to publish |
| `SUBMITTED` | One final click plus receipt/navigation/status evidence | Public visibility |
| `SCHEDULED` | Platform shows accepted scheduled time | Immediate publication |
| `REVIEWING` | Platform management surface shows review state for the matched item | Public visibility |
| `PUBLISHED` | Matched management item explicitly shows published/public status | Cross-platform completion for other rows |
| `BLOCKED` | Exact login/captcha/risk/permission/agreement gate is visible | Automatic recovery or bypass |

## Reporting template

For each selected platform record:

- account;
- task/video fingerprint;
- current state;
- final-click count;
- strongest evidence;
- remaining action, if any.

Do not collapse unresolved rows into a single success percentage.
