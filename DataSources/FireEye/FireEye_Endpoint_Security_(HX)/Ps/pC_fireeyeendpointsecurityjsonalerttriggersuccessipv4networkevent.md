#### Parser Content
```Java
{
Name = fireeye-endpointsecurity-json-alert-trigger-success-ipv4networkevent
    Vendor = FireEye
    Product = FireEye Endpoint Security (HX)
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """"hostname":""", """"event_at":""", """"event_type":""", """"ipv4NetworkEvent"""", """"ipv4NetworkEvent/remoteIP":""", """"alert_id":""", """"ipv4NetworkEvent/username":""" ]
    Fields = [
       """"event_at":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""",
       """"alert_id":\s*({alert_id}\d+)""",
       """"event_type":\s*"({alert_name}[^"]+)""",
       """"ipv4NetworkEvent/remoteIP":\s*"({dest_ip}[\da-fA-F.:]+)""",
       """"ipv4NetworkEvent/remotePort":\s*({dest_port}\d+)""",
       """"hostname":\s*"({host}[^"]+)""",
       """"ipv4NetworkEvent/processPath":\s*"({process_path}[^"]+)""",
       """"ipv4NetworkEvent/process":\s*"({process_name}[^"]+)""",
       """"ipv4NetworkEvent/protocol":\s*"({protocol}[^"]+)""",
       """"ipv4NetworkEvent/localIP":\s*"({src_ip}[\da-fA-F.:]+)""",
       """"ipv4NetworkEvent/localPort":\s*({src_port}\d+)""",
       """"ipv4NetworkEvent/username":\s*"(({domain}[^"\\\/]+)[\\\/]+)?({user}[^"]+)"""
    ]
    DupFields = ["alert_name->alert_type"]
	ParserVersion = "v1.0.0"
  

}
```