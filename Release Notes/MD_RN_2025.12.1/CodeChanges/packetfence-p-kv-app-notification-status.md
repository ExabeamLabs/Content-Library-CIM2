# Code Changes for packetfence-p-kv-app-notification-status (Parser)

| Code Change | Field Name | 2025.11.1 | 2025.12.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "packetfence-p-kv-app-notification-status", "Vendor": "PacketFence", "Product": "PacketFence", "ParserVersion": "v1.0.0", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["packetfence:", ", Status:"], "Fields": ["\s({host}[\w\-.]+)\s+packetfence:", "\s({app}packetfence)", "packetfence:\s*({event_category}\w+)", "packetfence:\s*.*?\[({src_mac}(\w{2}:){5}\w{2})", "PID:\s*\"({email_address}[^\s@\"]+@[^\s@\"]+)", "Status:\s*({action}\w+)"]} | N/A |