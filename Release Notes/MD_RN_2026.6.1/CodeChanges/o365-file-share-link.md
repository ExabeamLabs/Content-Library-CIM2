# Code Changes for o365-file-share-link (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'auth_type', 'browser', 'correlation_id', 'domain', 'email_address', 'file_ext', 'file_type', 'mailbox_name', 'object', 'object_id', 'object_type', 'operation', 'os', 'permissions', 'share_type', 'site_at', 'site_name', 'src_file_name', 'src_file_path', 'src_ip', 'src_port', 'target', 'target_domain', 'tenant_id', 'time', 'url', 'user', 'user_agent', 'user_sid', 'user_type', 'web_domain'] |
| edit_regex_field | object_type |  | ['"RecordType":\s*"*({object_type}[^,]+?)"*,', '"TargetUserOrGroupType":"({object_type}[^"]+)"'] |
| edit_regex_field | url |  | ['"SiteUrl":"({site_name}({url}[^"]+))"', 'exa_json_path=$.SiteUrl,exa_regex=({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)'] |
| added_regex_field | mailbox_name |  | ['"ObjectId\\*"{1,20}:"?[\s\\]*"+(Unknown|Not Available|({object}({mailbox_name}[^"]+)))', 'exa_regex="ObjectId\\*"{1,20}:"?[\s\\]*"+(Unknown|Not Available|({object}({mailbox_name}[^"]+)))'] |
| added_regex_field | object |  | ['"ObjectId\\*"{1,20}:"?[\s\\]*"+(Unknown|Not Available|({object}({mailbox_name}[^"]+)))', 'exa_regex="ObjectId\\*"{1,20}:"?[\s\\]*"+(Unknown|Not Available|({object}({mailbox_name}[^"]+)))'] |
| added_regex_field | permissions |  | ['<Type>({permissions}[^<\s]+?)<', 'exa_regex=<Type>({permissions}[^<\s]+?)<'] |
| added_regex_field | share_type |  | ['"Operation":"({share_type}[^"]+?)LinkCreated"', 'exa_regex="Operation":"({share_type}[^"]+?)LinkCreated"'] |
| added_regex_field | site_name |  | ['"SiteUrl":"({site_name}({url}[^"]+))"'] |
| added_regex_field | target |  | ['"TargetUserOrGroupName":"({target}[^"]+)"'] |
| added_regex_field | target_domain |  | ['"TargetUserOrGroupName":"([^@]+)@({target_domain}[^"]*?)"', 'exa_json_path=$.TargetUserOrGroupName,exa_regex=([^@]+)@({target_domain}[^"]*?)'] |