# Code Changes for packetfence-p-str-app-notification-cantfindprovisionerfor (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| removed_parser | N/A | {"Name": "packetfence-p-str-app-notification-cantfindprovisionerfor", "Vendor": "PacketFence", "Product": "PacketFence", "ParserVersion": "v1.0.0", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["packetfence:", "Can't find provisioner for"], "Fields": ["\s({host}[\w\-.]+)\s+packetfence:", "\s({app}packetfence)", "packetfence:\s*({event_category}\w+)", "({event_name}Can't find provisioner for ({src_mac}(\w{2}:){5}\w{2}))"]} | N/A |