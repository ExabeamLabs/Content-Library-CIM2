# Code Changes for dl-pan-ngfw-app-login-success (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'pan-gp-csv-vpn-login-useridlogin') && (!exists(result_code) || InList(toLower(result_code), '0x0')) |