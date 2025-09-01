# Code Changes for microsoft-evsecurity-xml-peripheral-storage-insert-success-devicewasrecognized (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | device_class |  | ['<Data Name=(\'|")ClassName(\'|")>({device_class}[^<]+)<', 'Class Name:\s+({device_class}[^:]+?)\s+(Vendor IDs:|Hardware IDs:)'] |
| edit_regex_field | device_pid |  | ['<Data Name=(\'|")DeviceId(\'|")>.+?VEN_({device_vid}[^&]+)&(amp;)?DEV_({device_pid}[^\\&]+)'] |
| edit_regex_field | device_vid |  | ['<Data Name=(\'|")DeviceId(\'|")>.+?VEN_({device_vid}[^&]+)&(amp;)?DEV_({device_pid}[^\\&]+)'] |