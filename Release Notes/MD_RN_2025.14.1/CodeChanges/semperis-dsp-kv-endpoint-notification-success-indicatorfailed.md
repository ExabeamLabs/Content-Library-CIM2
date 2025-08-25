# Code Changes for semperis-dsp-kv-endpoint-notification-success-indicatorfailed (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "semperis-dsp-kv-endpoint-notification-success-indicatorfailed", "Vendor": "Semperis", "Product": "Semperis DSP", "ParserVersion": "v1.0.0", "TimeFormat": "yyyy-MM-dd'T'HH:mm:ss.SSS", "Conditions": ["Security indicator failed to run:", "Result: ", "Forest name:"], "Fields": ["({event_name}Security indicator failed to run)", "Result:\s*({result}[\S]+)", "Domains:\s*({domain}[^:]+?)\s\w+?:", "Severity:\s*({alert_severity}[^:]+?)\s\w+?:", "Security indicator failed to run:\s*({additional_info}[^:]+?)\s+Generation time:"]} | N/A |