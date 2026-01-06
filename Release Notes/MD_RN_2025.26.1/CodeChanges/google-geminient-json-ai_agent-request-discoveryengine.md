# Code Changes for google-geminient-json-ai_agent-request-discoveryengine (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['app_id', 'email_address', 'email_domain', 'src_ip', 'src_port'] |
| edit_regex_field | email_address |  | ['exa_json_path=$..authenticationInfo.principalEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'exa_json_path=$..authenticationInfo.principalSubject,exa_regex=[^\\,]+\/({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| edit_regex_field | email_domain |  | ['exa_json_path=$..authenticationInfo.principalEmail,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))', 'exa_json_path=$..authenticationInfo.principalSubject,exa_regex=[^\\,]+\/({email_address}([A-Za-z0-9]+[!#$%&\'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))'] |
| added_regex_field | app_id |  | ['exa_regex="resourceName":[^\]\},]+?engines\/({app_id}[^\/,]+?)\/'] |