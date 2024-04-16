#### Parser Content
```Java
{
Name = unix-unix-str-network-start-snmpd
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """]: Connection from """, """snmpd""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-.]+)(\s\w+)?\s({event_name}[^\[]+)\s*\[({process_id}[^\]]+)\]:\s*Connection from ({protocol}[^\:\s]+):\s*\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]:({src_port}\d+)->\[({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\]""",
  ]
  ParserVersion = "v1.0.0"


}
```