#### Parser Content
```Java
{
Name = apc-a-str-app-logout-success-loggedout
  ParserVersion = v1.0.0
  Vendor = APC
  Product = APC
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [  """ Web user """, """ logged out from """ ]
  Fields = [
    """<\d+>(\w+\s+\d+\s+\d\d:\d\d:\d\d)\s+({host}[\w.\-]+)\s""",
    """"@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """Web user '({user}[\w\.\-]{1,40}\$?)'""",
    """\slogged out from ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\.?\s+"""
  ]
  DupFields = [ "host->dest_host" ]


}
```