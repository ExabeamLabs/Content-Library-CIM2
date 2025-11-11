# Code Changes for pan-prismaaccess-leef-network-traffic-fail-deny (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | action |  | ['EventStatus=({action}({result}[^\s=]+))', '\sAction=({action}({result}[^=]+?))\s\w+=', '\|Prisma Access\|[^\|]+\|({action}[^\|]+)\|'] |
| edit_regex_field | result |  | ['EventStatus=({action}({result}[^\s=]+))', '\sAction=({action}({result}[^=]+?))\s\w+='] |
| removed_attribute | DupFields |  | N/A |