#### Parser Content
```Java
{
Name = fireeye-endpointsecurity-json-alert-trigger-success-processevent
    Vendor = FireEye
    Product = FireEye Endpoint Security (HX)
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """"event_at":""", """"event_type":""", """"processEvent"""", """"processEvent/pid":""", """"processEvent/process":""", """"alert_id":""" ]
    Fields = [
       """"event_at":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
       """"alert_id":\s*({alert_id}\d+)""",
       """"processEvent/eventType":\s*"({event_name}[^"]+)""",
       """"processEvent/processCmdLine":\s*"({process_command_line}.+?)"\}?,""",
       """"last_poll_ip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
       """"hostname":\s*"({host}[^"]+)""",
       """"processEvent/md5":\s*"({hash_md5}[^"]+)""",
       """"processEvent/process":\s*"({process_name}[^"]+)""",
       """"processEvent/username":\s*"(({domain}[^"\\\/]+)[\\\/]+)?({user}[\w\.\-]{1,40}\$?)"""
       """"event_type":\s*"({alert_name}[^"]+)"""
    ]
    DupFields = ["alert_name->alert_type"]
	ParserVersion = "v1.0.0"


}
```