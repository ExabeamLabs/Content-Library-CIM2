#### Parser Content
```Java
{
Name = microsoft-windows-kv-dhcp-session-success-assign
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft DHCP Log
  TimeFormat = "dd/MM/yyyy:HH:mm:ss z"
  Conditions = [ """WindowsDHCP""", """Description=Assign""" ]
  Fields = [
    """IP Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Host Name =({dest_host}[\w\-.]+)"""
    """"UtcTime"="({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d \w+)""""
  ]
  DupFields = [ "dest_host->user" ]


}
```