# Code Changes for microsoft-o365-sk4-file-app-userkey (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'email_address', 'email_domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'object', 'object_id', 'object_type', 'operation', 'policy_name', 'removable_media_serial_number', 'removable_media_vendor', 'src_file_ext', 'src_file_name', 'src_file_path', 'src_host', 'src_ip', 'src_port', 'time', 'url', 'user_agent', 'user_type', 'web_domain'] |
| added_regex_field | url |  | ['"SiteUrl":\s*"({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)', 'exa_json_path=$.SiteUrl,exa_regex=({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)'] |
| added_regex_field | web_domain |  | ['"SiteUrl":\s*"({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)', 'exa_json_path=$.SiteUrl,exa_regex=({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)'] |