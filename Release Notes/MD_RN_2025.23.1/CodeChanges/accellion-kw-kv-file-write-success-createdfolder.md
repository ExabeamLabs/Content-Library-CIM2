# Code Changes for accellion-kw-kv-file-write-success-createdfolder (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['access', 'bytes', 'dest_host', 'dest_ip', 'dest_port', 'email_address', 'email_domain', 'file_ext', 'file_name', 'host', 'operation', 'src_file_ext', 'src_file_name', 'src_ip', 'src_port'] |
| edit_regex_field | access |  | ['({access}Created) folder ({file_name}({src_file_name}[^$"\.]+?(\.(|({file_ext}({src_file_ext}[^$"]+?))))?))\.?\s*(File:|$)', '({access}Created) folder \"+({file_name}({src_file_name}[^\"\.]+?(\.({file_ext}({src_file_ext}[^"]+)))?))\"'] |
| edit_regex_field | src_file_ext |  | ['({access}Created) folder ({file_name}({src_file_name}[^$"\.]+?(\.(|({file_ext}({src_file_ext}[^$"]+?))))?))\.?\s*(File:|$)', '({access}Created) folder \"+({file_name}({src_file_name}[^\"\.]+?(\.({file_ext}({src_file_ext}[^"]+)))?))\"'] |
| edit_regex_field | src_file_name |  | ['({access}Created) folder ({file_name}({src_file_name}[^$"\.]+?(\.(|({file_ext}({src_file_ext}[^$"]+?))))?))\.?\s*(File:|$)', '({access}Created) folder \"+({file_name}({src_file_name}[^\"\.]+?(\.({file_ext}({src_file_ext}[^"]+)))?))\"'] |
| added_regex_field | file_ext |  | ['({access}Created) folder ({file_name}({src_file_name}[^$"\.]+?(\.(|({file_ext}({src_file_ext}[^$"]+?))))?))\.?\s*(File:|$)', '({access}Created) folder \"+({file_name}({src_file_name}[^\"\.]+?(\.({file_ext}({src_file_ext}[^"]+)))?))\"'] |
| added_regex_field | file_name |  | ['({access}Created) folder ({file_name}({src_file_name}[^$"\.]+?(\.(|({file_ext}({src_file_ext}[^$"]+?))))?))\.?\s*(File:|$)', '({access}Created) folder \"+({file_name}({src_file_name}[^\"\.]+?(\.({file_ext}({src_file_ext}[^"]+)))?))\"'] |
| removed_attribute | DupFields |  | N/A |