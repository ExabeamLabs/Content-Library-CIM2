#### Parser Content
```Java
{
Name = microsoft-windows-kv-dhcp-session-success-assign
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "epoch"
  Conditions = [ """WindowsDHCP""", """Description=Assign""" ]
  Fields = [
    """IP Address=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """Host Name =({dest_host}[^\s]+)"""
  ]
  DupFields = [ "dest_host->user" ]


}
```