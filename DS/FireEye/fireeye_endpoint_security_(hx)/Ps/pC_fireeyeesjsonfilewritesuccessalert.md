#### Parser Content
```Java
{
Name = "fireeye-es-json-file-write-success-alert"
Vendor = "FireEye"
Product = "FireEye Endpoint Security (HX)"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""hostname":"""
""""event_at":"""
""""event_type":"""
""""fileWriteEvent""""
""""fileWriteEvent/fileName":"""
""""alert_id":"""
]
Fields = [
""""event_at":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
""""alert_id":\s*({alert_id}\d+)"""
""""last_poll_ip":\s*"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
""""event_id":\s*({event_code}\d+)"""
""""fileWriteEvent/eventReason":\s*"({operation}[^"]+)"""
""""fileWriteEvent/fileName":\s*"({file_name}[^"]+)"""
""""hostname":\s*"({host}[^"]+)"""
""""fileWriteEvent/username":\s*"(({domain}[^"\\\/]+)[\\\/]+)?({user}[^"]+)"""
""""event_type":\s*"({event_name}[^"]+)"""
""""fileWriteEvent\/fullPath":\s*"({file_path}[^"]+)"""
""""fileWriteEvent\/process":\s*"({process_path}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```