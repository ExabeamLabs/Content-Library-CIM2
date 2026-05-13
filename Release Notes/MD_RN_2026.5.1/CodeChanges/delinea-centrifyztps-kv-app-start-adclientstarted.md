# Code Changes for delinea-centrifyztps-kv-app-start-adclientstarted (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "delinea-centrifyztps-kv-app-start-adclientstarted", "Vendor": "Delinea", "Product": "Centrify Zero Trust Privilege Services", "TimeFormat": "epoch_sec", "Conditions": ["|Centrify Suite|DirectControl UNIX Agent|", "started|"], "Fields": ["utc=({time}\d{10})", "\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w.\-]+)\s", "user=({user}[\w\.\-\!\#\^\~]{1,40}\$?)", "\d+\|\d+\|({event_name}.+?)\|\d", "status=({result}.+?)\s\w+=", "pid=({process_id}\d+)", "service=({service_name}.+?)$", "centrifyEventID=({event_code}\d+)"], "ParserVersion": "v1.0.0"} |