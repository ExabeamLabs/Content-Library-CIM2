# Code Changes for microsoft-evterminalservicesgateway-str-rdp-traffic-success-connectedtoresource (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| changed_parsed_fields | N/A |  | ['channel', 'dest_host', 'dest_ip', 'domain', 'protocol', 'src_ip', 'src_port', 'user'] |
| added_regex_field | channel |  | ['<Channel>({channel}[^<]+)<'] |