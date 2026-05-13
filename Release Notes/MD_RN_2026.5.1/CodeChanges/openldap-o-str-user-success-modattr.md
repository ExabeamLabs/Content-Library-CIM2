# Code Changes for openldap-o-str-user-success-modattr (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['account_name', 'attribute', 'auth_method', 'connection_id', 'dest_user', 'dest_user_dn', 'domain_controller', 'host', 'operation', 'operation_id', 'profile', 'technique'] |
| edit_regex_field | dest_user |  | ['(uid=({dest_user}({account_name}[^,]+))|cn=({=dest_user}({=account_name}[^,]+))),ou=(?i:(users|people|employees|staff|members|accounts|endusers|sudoers))'] |
| added_regex_field | account_name |  | ['(uid=({dest_user}({account_name}[^,]+))|cn=({=dest_user}({=account_name}[^,]+))),ou=(?i:(users|people|employees|staff|members|accounts|endusers|sudoers))'] |