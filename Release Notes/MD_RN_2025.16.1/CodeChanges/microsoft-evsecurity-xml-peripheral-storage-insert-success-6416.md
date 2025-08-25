# Code Changes for microsoft-evsecurity-xml-peripheral-storage-insert-success-6416 (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | device_pid |  | ['<Data Name=(\'|")DeviceId(\'|")>USB\\+VID_({device_vid}[^&]+)&(amp;)?PID_({device_pid}[^\\&]+)'] |
| edit_regex_field | device_vid |  | ['<Data Name=(\'|")DeviceId(\'|")>USB\\+VID_({device_vid}[^&]+)&(amp;)?PID_({device_pid}[^\\&]+)'] |