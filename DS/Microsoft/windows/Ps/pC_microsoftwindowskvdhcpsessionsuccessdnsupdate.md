#### Parser Content
```Java
{
Name = microsoft-windows-kv-dhcp-session-success-dnsupdate
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "dd/MM/yyyy:HH:mm:ss z"
  Conditions = [ """Description=DNS Update Successful""", """Host Name =""", """QResult=""" ]
  Fields = [
    """<.*?>\w+ \d+ \d+:\d+:\d+\s+({host}[^\s]+)""",
    """\sIP Address=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\sHost Name =({dest_host}[\w.\-]+)""",
    """"UtcTime"="({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d \w+)""""
  ]
  DupFields = [ "dest_host->user" ]


}
```