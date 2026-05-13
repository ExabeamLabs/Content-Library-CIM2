# Code Changes for microsoft-o365-json-email-send-receive-internentmessageid (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'additional_info', 'alert_id', 'alert_name', 'alert_type', 'app', 'attachment', 'confidence_level', 'dest_email_address', 'dest_email_folder', 'direction', 'email_address', 'email_recipients', 'email_subject', 'email_user', 'file_ext', 'file_name', 'hash_sha256', 'malware_action', 'result', 'src_email_folder', 'src_ip', 'src_port', 'time', 'user_type'] |
| edit_regex_field | dest_email_address |  | ['"Recipients":\[?"({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"?\]?'] |
| edit_regex_field | email_address |  | ['"P1Sender":"((([^@]+?\\=)+)?({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({email_user}[^"]+))"', '"P2Sender":"((([^@]+?\\=)+)?({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({email_user}[^"]+))"'] |
| edit_regex_field | email_recipients |  | ['"Recipients":\[?"({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"?\]?'] |
| edit_regex_field | email_user |  | ['"P1Sender":"((([^@]+?\\=)+)?({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({email_user}[^"]+))"', '"P2Sender":"((([^@]+?\\=)+)?({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({email_user}[^"]+))"'] |
| added_regex_field | confidence_level |  | ['"PhishConfidenceLevel":"({confidence_level}[^"]+)"'] |
| added_regex_field | dest_email_folder |  | ['"LatestDeliveryLocation":"({dest_email_folder}[^"]+)"'] |
| added_regex_field | malware_action |  | ['"PolicyAction":"({malware_action}[^"]+)"'] |
| added_regex_field | src_email_folder |  | ['"OriginalDeliveryLocation":"({src_email_folder}[^"]+)"'] |