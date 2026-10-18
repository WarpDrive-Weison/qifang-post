# Evidence model

Use the strongest independently observed state and keep lower states distinct.

| State | Minimum evidence | Do not claim |
| --- | --- | --- |
| `PREPARED` | Local video and metadata recorded in the Mac app or Windows local task record | Platform upload started |
| `UPLOADING` | Platform accepted the file and transport is active | A trustworthy percentage when none is exposed |
| `UPLOADED` | Platform reports transport complete | Form complete or submitted |
| `FORM_READY` | Video and every required fingerprinted field read back correctly | Permission to publish |
| `SUBMITTED` | One final click plus receipt/navigation/status evidence | Public visibility |
| `SCHEDULED` | Platform shows accepted scheduled time | Immediate publication |
| `REVIEWING` | Platform management surface shows review state for the matched item | Public visibility |
| `PUBLISHED` / 发布成功 | After submission, complete same title in the current account's visible management work item (Mac title-match rule) | Review approval, public visibility, unique upload attribution, or other platform completion |
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
