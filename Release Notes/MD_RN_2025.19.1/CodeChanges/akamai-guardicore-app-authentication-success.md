# Code Changes for akamai-guardicore-app-authentication-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'akamai-guardicore-cef-app-activity-userauth') && InList(toLower(action), 'user authentication') && containsAny(toLower(additional_info), 'successful','passed') |