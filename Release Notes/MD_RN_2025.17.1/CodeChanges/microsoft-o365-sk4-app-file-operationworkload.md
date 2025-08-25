# Code Changes for microsoft-o365-sk4-app-file-operationworkload (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'additional_info', 'alert_severity', 'app', 'app_id', 'browser', 'bytes_in', 'correlation_id', 'dest_domain', 'dest_email_address', 'domain', 'email_address', 'email_domain', 'failure_reason', 'file_ext', 'file_name', 'host', 'login_type', 'object', 'object_id', 'operation', 'os', 'process_name', 'resource', 'result', 'role_name', 'session_id', 'src_host', 'src_ip', 'src_port', 'target', 'time', 'user', 'user_agent', 'user_sid', 'user_type', 'user_upn'] |
| edit_regex_field | host |  | ['"OriginatingServer":"({host}[\w\-.]+?)\s*\(', '"Target"[^\]]+"Device"[^\]]+"ID":"({host}[\w\-.]+)"', '"host\\*"+:[\s\\]*"+({host}[^"\\]+)', '\sdvc=({host}\S+)', '\sdvchost=(Unknown|({host}[\w\-.]+))'] |
| edit_regex_field | src_host |  | ['"DeviceProperties":\s*\[\{[^\]]+?(("Value":\s*"({src_host}[^"]+)",\s*"Name":\s*"DisplayName")|("Name":\s*"DisplayName",\s*"Value":\s*"({=src_host}[^"]+)"))\},', '("Device\.DisplayName"[^\}]*?"NewValue":"({src_host}[\w\-\.]+)",)|("NewValue":"({=src_host}[\w\-\.]+)",[^\}]*?"Device\.DisplayName")'] |
| added_regex_field | login_type |  | ['"InternalLogonType":({login_type}\d+)'] |