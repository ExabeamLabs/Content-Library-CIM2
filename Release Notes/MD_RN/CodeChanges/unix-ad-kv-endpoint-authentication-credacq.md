# Code Changes for unix-ad-kv-endpoint-authentication-credacq (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed | Conditions | ['PAM:setcred', 'type=CRED_ACQ'] | ['CRED_ACQ', 'PAM:setcred'] |