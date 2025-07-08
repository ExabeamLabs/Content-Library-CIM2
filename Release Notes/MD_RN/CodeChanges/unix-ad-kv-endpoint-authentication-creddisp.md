# Code Changes for unix-ad-kv-endpoint-authentication-creddisp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions | ['PAM:setcred', 'type=CRED_DISP'] | ['CRED_DISP', 'PAM:setcred'] |