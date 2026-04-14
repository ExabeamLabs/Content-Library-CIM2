# Code Changes for forcepoint-dlp-cef-alert-trigger-success-forcepointdlp (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | bytes |  | ['\Wfname=(N\/A|.*? - ({bytes}[\d.]+)\s+({bytes_unit}\w+))\s\w+='] |
| edit_regex_field | bytes_unit |  | ['\Wfname=(N\/A|.*? - ({bytes}[\d.]+)\s+({bytes_unit}\w+))\s\w+='] |
| edit_regex_field | bytes_val |  | ['\Wfname=(N\/A|.*? - ({bytes_val}[\d\.]+\s+[^\s;]+))\s\w+='] |