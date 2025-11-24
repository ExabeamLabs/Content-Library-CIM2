# Code Changes for kaspersky-endpointsecurity-xml-alert-trigger-success-security (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['alert_name', 'alert_type', 'domain', 'file_dir', 'file_ext', 'file_name', 'file_path', 'group_name', 'result', 'src_host', 'src_ip', 'src_port', 'threat_category', 'time', 'user'] |
| edit_regex_field | alert_name |  | ['<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){3}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>({alert_type}({alert_name}[^\<]+?))<\/Data><\/Cell>'] |
| added_regex_field | alert_type |  | ['<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){3}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>({alert_type}({alert_name}[^\<]+?))<\/Data><\/Cell>'] |
| removed_attribute | DupFields |  | N/A |