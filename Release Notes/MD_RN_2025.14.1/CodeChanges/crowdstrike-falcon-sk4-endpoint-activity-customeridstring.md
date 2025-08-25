# Code Changes for crowdstrike-falcon-sk4-endpoint-activity-customeridstring (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| changed_parsed_fields | N/A | ['event_name', 'hash_sha256', 'time', 'user'] | ['cid', 'event_name', 'hash_sha256', 'object_dn', 'time', 'user'] |
| added_regex_field | cid | [] | ['"cid":"({cid}[^"]+)"'] |
| added_regex_field | object_dn | [] | ['"IssuerDN":"({object_dn}[^"]+)"'] |