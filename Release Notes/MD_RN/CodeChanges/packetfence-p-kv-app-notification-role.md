# Code Changes for packetfence-p-kv-app-notification-role (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| removed_parser | N/A | {"Name": "packetfence-p-kv-app-notification-role", "Vendor": "PacketFence", "Product": "PacketFence", "ParserVersion": "v1.0.0", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["packetfence:", " role:"], "Fields": ["\s({host}[\w\-.]+)\s+packetfence:", "\s({app}packetfence)", "packetfence:\s*({event_category}\w+)", "packetfence:\s*.*?\[({src_mac}(\w{2}:){5}\w{2})", "Returning\s+({action}\w+)", "role:\s*({role}\S+)"]} | N/A |