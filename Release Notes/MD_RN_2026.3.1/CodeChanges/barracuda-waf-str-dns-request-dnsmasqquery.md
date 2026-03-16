# Code Changes for barracuda-waf-str-dns-request-dnsmasqquery (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_attribute | Vendor |  | Simon Kelley |
| edit_attribute | Product |  | Dnsmasq |
| changed_parsed_fields | N/A |  | ['app', 'dns_query', 'host', 'src_ip', 'time'] |
| edit_regex_field | time |  | ['({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+\s*(\+|\-)[\d:]+)\s({host}[\w\-.]+)\sdnsmasq'] |
| added_regex_field | host |  | ['({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+\s*(\+|\-)[\d:]+)\s({host}[\w\-.]+)\sdnsmasq'] |
| edit_attribute | legacy_product |  | ['Dnsmasq'] |