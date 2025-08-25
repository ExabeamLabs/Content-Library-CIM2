# Code Changes for packetfence-p-str-app-notification-connectiontypeiswirelessmacauth (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "packetfence-p-str-app-notification-connectiontypeiswirelessmacauth", "Vendor": "PacketFence", "Product": "PacketFence", "ParserVersion": "v1.0.0", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["packetfence:", "Connection type is WIRELESS_MAC_AUTH"], "Fields": ["\s({host}[\w\-.]+)\s+packetfence:", "\s({app}packetfence)", "packetfence:\s*({event_category}\w+)", "packetfence:\s*.*?\[({src_mac}(\w{2}:){5}\w{2})", "packetfence:\s*\w+\s+\S+\s+\S+\s+({event_name}[^\[\]:\"\-\.]+)"]} | N/A |