# Code Changes for checkpoint-endpointsecurity-alert-trigger-success-1 (Event Builder)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_conditions | expression |  | InList(type, 'checkpoint-tp-kv-alert-trigger-success-actiondetect') && containsAny(toLower(product_name), 'anti malware','new anti virus','smartdefense','threat emulation','url filtering','zero phishing','threat extraction','vpn-1 & firewall-1','anti-spam & email security','anti-bot','data loss prevention','ips','anti-virus','application control','content awareness','identity awareness','mobile access','compliance') |