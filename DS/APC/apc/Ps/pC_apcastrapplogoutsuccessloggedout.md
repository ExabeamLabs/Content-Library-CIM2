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
    """Web user '({user}[^']+)'""",
    """\slogged out from ({src_ip}[a-fA-F\d.:]+?)\.?\s+"""
  ]
  DupFields = [ "host->dest_host" ]


}
```