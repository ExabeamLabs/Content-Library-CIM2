# Code Changes for google-cloudplatform-json-app-database-success-database (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app', 'db_name', 'db_query', 'db_user', 'region', 'resource_dir', 'resource_name', 'resource_path', 'service_name', 'time'] |
| added_regex_field | resource_dir |  | ['exa-regex=resourceName":\s*"({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))"'] |
| added_regex_field | resource_name |  | ['exa-regex=resourceName":\s*"({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))"'] |
| added_regex_field | resource_path |  | ['exa-regex=resourceName":\s*"({resource_path}({resource_dir}[^"]+)\/({resource_name}[^"\/]+))"'] |
| added_attribute | ExtractionType |  | json |