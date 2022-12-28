#### Parser Content
```Java
{
Name = unix-unix-str-network-start-snmpd
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """]: Connection from """, """snmpd""" ]
  Fields = [
    """\d\d:\d\d:\d\d ({host}[\w\-.]+) ({event_name}[^\[]+)\s*\[({process_id}[^\]]+)\]:\s*Connection from ({protocol}[^\:\s]+):\s*\[({src_ip}[A-Fa-f:\d.]+)\]:({src_port}\d+)->\[({dest_ip}[A-Fa-f:\d.]+)\]""",
  ]
  ParserVersion = "v1.0.0"


}
```