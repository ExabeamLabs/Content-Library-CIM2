# Code Changes for microsoft-azure-json-image-write-success-createvm (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['computer_name', 'email_address', 'email_domain', 'first_name', 'full_name', 'image_name', 'image_publisher', 'image_release', 'image_version', 'instance_id', 'interface_id', 'last_name', 'operation_first', 'operation_last', 'os_admin', 'os_type', 'region', 'resource', 'resource_group', 'resource_id', 'resource_name', 'resource_path', 'src_ip', 'src_port', 'src_resource', 'src_resource_type', 'subscription_id', 'user', 'user_upn', 'vm_size'] |
| edit_regex_field | image_name |  | ['exa_json_path=$..responseBody,exa_regex="imageReference\\?"+:[^\}]+"+offer\\?"+:\s*\\?"+({src_resource}({image_name}[^"]+))\\?"'] |
| added_regex_field | src_resource |  | ['exa_json_path=$..responseBody,exa_regex="imageReference\\?"+:[^\}]+"+offer\\?"+:\s*\\?"+({src_resource}({image_name}[^"]+))\\?"'] |
| removed_attribute | DupFields |  | N/A |