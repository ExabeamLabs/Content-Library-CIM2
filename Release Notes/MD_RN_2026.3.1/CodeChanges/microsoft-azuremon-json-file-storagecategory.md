# Code Changes for microsoft-azuremon-json-file-storagecategory (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['category', 'correlation_id', 'file_ext', 'file_name', 'file_path', 'location', 'operation', 'protocol', 'region', 'resource_id', 'resource_type', 'result', 'result_code', 'service_name', 'service_type', 'src_ip', 'src_port', 'storage_account', 'time', 'url', 'user_agent'] |
| edit_regex_field | file_name |  | ['"uri":"+({url}({file_path}[^"]+\\/?({file_name}[^\\?"\.]+(\.({file_ext}[^"\\]+))?))[^"]*|[^"]+)"'] |
| edit_regex_field | file_path |  | ['"uri":"+({url}({file_path}[^"]+\\/?({file_name}[^\\?"\.]+(\.({file_ext}[^"\\]+))?))[^"]*|[^"]+)"'] |
| edit_regex_field | url |  | ['"uri":"+({url}({file_path}[^"]+\\/?({file_name}[^\\?"\.]+(\.({file_ext}[^"\\]+))?))[^"]*|[^"]+)"'] |
| added_regex_field | file_ext |  | ['"uri":"+({url}({file_path}[^"]+\\/?({file_name}[^\\?"\.]+(\.({file_ext}[^"\\]+))?))[^"]*|[^"]+)"'] |
| edit_attribute | activity_type |  | ['app-activity:success', 'database-create:success', 'database-delete:success', 'database-query:success', 'file-create:success', 'file-delete:success', 'file-list:fail', 'file-list:success', 'file-permission-read:success', 'file-property-modify:success', 'file-property-read:success', 'file-read:success', 'file-write:success', 'share-create:success', 'share-delete:success', 'share-modify:success', 'snapshot-modify:success'] |