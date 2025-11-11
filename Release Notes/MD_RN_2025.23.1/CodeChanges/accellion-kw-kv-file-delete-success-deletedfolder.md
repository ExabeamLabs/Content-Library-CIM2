# Code Changes for accellion-kw-kv-file-delete-success-deletedfolder (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'bytes', 'dest_host', 'email_address', 'email_domain', 'file_ext', 'file_name', 'host', 'operation', 'src_ip', 'src_port'] |
| edit_regex_field | host |  | ['({dest_host}({host}[\w.\-]+))\s+rest_server.py:', '\w+\s+\d+ \d+:\d+:\d+\s+({dest_host}({host}[\w.\-]+))\s+'] |
| added_regex_field | dest_host |  | ['({dest_host}({host}[\w.\-]+))\s+rest_server.py:', '\w+\s+\d+ \d+:\d+:\d+\s+({dest_host}({host}[\w.\-]+))\s+'] |
| removed_attribute | DupFields |  | N/A |