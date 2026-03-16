# Code Changes for barracuda-waf-str-dns-response-dnsmasqcached (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | Vendor |  | Simon Kelley |
| edit_attribute | Product |  | Dnsmasq |
| changed_parsed_fields | N/A |  | ['app', 'dest_ip', 'dns_query', 'host', 'time'] |
| edit_regex_field | time |  | ['({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+\s*(\+|\-)[\d:]+)\s({host}[\w\-.]+)\sdnsmasq'] |
| added_regex_field | host |  | ['({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+\s*(\+|\-)[\d:]+)\s({host}[\w\-.]+)\sdnsmasq'] |
| edit_attribute | legacy_product |  | ['Dnsmasq'] |