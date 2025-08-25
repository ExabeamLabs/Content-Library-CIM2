# Code Changes for qualys-vmdr-kv-app-activity-success-event (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| added_parser | N/A |  | {"Name": "qualys-vmdr-kv-app-activity-success-event", "Vendor": "Qualys", "Product": "Qualys AssetView", "TimeFormat": "MMM dd HH:mm:ss", "Conditions": ["katana[", "SCANNER='", "CAT='TARGET'", "EVENT='"], "Fields": ["\sIPV4='({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?'", "\sSCANNER='({additional_info}[^']+)", "\sCAT='({category}[^']+)", "\sEVENT='({event_name}[^']+)", "\s({process_name}katana)\[({process_id}\d+)\]", "({time}\w{3} \d\d \d\d:\d\d:\d\d)"], "DupFields": ["event_name->operation"], "ParserVersion": "v1.0.0"} |