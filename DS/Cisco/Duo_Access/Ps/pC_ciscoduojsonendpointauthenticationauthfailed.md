#### Parser Content
```Java
{
Name = cisco-duo-json-endpoint-authentication-authfailed
  Vendor = Cisco
  Product = Duo Access
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [""""server_section":""", """"auth_stage":""", """authentication"""]
  Fields = [
    """\sdvchost=({host}[\w\-.]+)\s\w+=""",
    """"hostname":\s*"({host}[\w\-.]+)"""",
    """"username":\s*"(|({user}[^"]+))"""",
    """"status":\s*"(|({action}[^"]+))"""",
    """"client_ip":\s*"({src_ip}[A-Fa-f\d:.]+)"""",
    """(("status":\s*"Reject"[^\}]*"msg":\s*"({failure_reason}[^"]+))|("msg":\s*"({additional_info}[^"]+)))"""",
    """"timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """"auth_stage":\s*"(|({auth_method}[^"]+))""""
  ]
  ParserVersion = "v1.0.0"


}
```