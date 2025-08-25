# Code Changes for amazon-awscloudwatch-cef-network-traffic-success-cloudwatch (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['action', 'aws_account', 'bytes', 'category', 'dest_ip', 'dest_port', 'protocol', 'region', 'service_name', 'src_ip', 'src_port', 'time', 'user'] |
| added_regex_field | region |  | ['\WResources":.+?"Region":"({region}[^"]+)"'] |