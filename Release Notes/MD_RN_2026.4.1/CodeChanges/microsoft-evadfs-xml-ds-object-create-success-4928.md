# Code Changes for microsoft-evadfs-xml-ds-object-create-success-4928 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'ds_object_dn', 'event_code', 'host', 'naming_context', 'options', 'process_id', 'result', 'result_code', 'run_level', 'src_ds_object_dn', 'src_host', 'sub_category', 'thread_id', 'time'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |