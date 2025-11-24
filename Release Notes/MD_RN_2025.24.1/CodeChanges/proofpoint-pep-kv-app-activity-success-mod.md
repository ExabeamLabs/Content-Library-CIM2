# Code Changes for proofpoint-pep-kv-app-activity-success-mod (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'alert_id', 'bytes', 'command', 'email_address', 'email_domain', 'file_name', 'hash_sha256', 'host', 'malware_score', 'original_risk_score', 'phishing_score', 'policy_name', 'protocol', 'rule', 'spam_score', 'src_ip', 'src_port', 'time', 'user', 'xid'] |
| edit_regex_field | xid |  | ['\sx=({alert_id}({xid}[^\s]+))\s'] |
| added_regex_field | alert_id |  | ['\sx=({alert_id}({xid}[^\s]+))\s'] |
| removed_attribute | DupFields |  | N/A |