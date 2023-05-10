#### Parser Content
```Java
{
Name = fireeye-escm-json-alert-trigger-success-fireeyecm
  Vendor = FireEye
  Product = FireEye Endpoint Security (CM)
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"FireEyeCM"""", """"NX"""", """"malwareName":"""", """"malwareSType":"""" ]
  Fields = [
    """"@timestamp":"({time}\d\d\d\d\-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"deviceIP":"({host}[A-Fa-f:\d.]+)""",
    """"srcIP":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"dstIP":"({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"alertURL":"({malware_url}[^"]+)""",
    """"malwareName":\s*"({alert_name}[^"]+)""",
    """"malwareSType":"({alert_type}[^"]+)""",
    """"srcHostname":"({src_host}[\w\-.]+)""",
    """"severity":"({alert_severity}[^"]+)""",
    """"deviceSensor":"({sensor}[^"]+)""",
    """"protocol":"({protocol}[^"]+)""",
    """"srcPort":"({src_port}\d+)""",
  ]
  ParserVersion = "v1.0.0"


}
```