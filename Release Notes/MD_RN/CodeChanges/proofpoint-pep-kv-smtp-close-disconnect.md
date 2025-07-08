# Code Changes for proofpoint-pep-kv-smtp-close-disconnect (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A | ['action', 'bytes', 'command', 'email_address', 'email_domain', 'file_name', 'hash_md5', 'host', 'malware_score', 'original_risk_score', 'phishing_score', 'policy_name', 'protocol', 'rule', 'spam_score', 'src_ip', 'src_port', 'time', 'user', 'xid'] | ['action', 'bytes', 'command', 'email_address', 'email_domain', 'file_name', 'hash_sha256', 'host', 'malware_score', 'original_risk_score', 'phishing_score', 'policy_name', 'protocol', 'rule', 'spam_score', 'src_ip', 'src_port', 'time', 'user', 'xid'] |
| removed_regex_field | hash_md5 | ['sha256=(?:\s|({hash_md5}[^\s]+))\s'] | [] |
| added_regex_field | hash_sha256 | [] | ['sha256=(?:\s|({hash_sha256}[^\s]+))\s'] |