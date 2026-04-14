# Code Changes for google-cloudplatform-json-role-modify-success-googleiamupdaterole (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['bucket_name', 'email_address', 'email_domain', 'event_category', 'failure_reason', 'operation', 'operation_first', 'operation_last', 'operation_type', 'permission', 'permissions', 'policy_bindings', 'project_id', 'region', 'resource_dir', 'resource_name', 'resource_path', 'resource_type', 'result_code', 'service_name', 'severity', 'src_ip', 'src_port', 'tag', 'time', 'user_agent', 'zone'] |
| added_regex_field | permissions |  | ['exa_json_path=$.protoPayload.serviceData.permissionDelta.addedPermissions,exa_regex=\[({permissions}[^\]]+)\]'] |