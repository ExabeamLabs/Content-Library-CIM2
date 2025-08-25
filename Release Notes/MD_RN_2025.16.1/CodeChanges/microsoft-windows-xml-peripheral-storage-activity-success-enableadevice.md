# Code Changes for microsoft-windows-xml-peripheral-storage-activity-success-enableadevice (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | device_pid |  | ['<Data Name=(\'|")DeviceId(\'|")>USB\\+VID_({device_vid}[^&]+)&(amp;)?PID_({device_pid}[^\\&]+)'] |
| edit_regex_field | device_vid |  | ['<Data Name=(\'|")DeviceId(\'|")>USB\\+VID_({device_vid}[^&]+)&(amp;)?PID_({device_pid}[^\\&]+)'] |