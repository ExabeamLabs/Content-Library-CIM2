# Code Changes for netskope-sc-json-network-traffic-traffictype (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | action |  | ['"action":\s*"({action}[^"]+)', '\"+bypass_reason\"+:\s*\"+({action}[^\",]+)'] |