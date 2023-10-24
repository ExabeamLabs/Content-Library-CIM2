#### Parser Content
```Java
{
Name = pan-tesm-csv-app-notification-success-validationfailed
  Vendor = Palo Alto Networks
  Product = Traps Endpoint Security Manager
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """,Traps""", """,Machine License Validation Failed,""" ]
  Fields = [
    """\d\d:\d\d ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))? .+?({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d),([^,]*,){3}({event_name}Machine License Validation Failed),({src_host}[^,]+),(|({user}[\w\.\-]{1,40}\$?)),({host}[^,]+)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  DupFields = [ "host->dest_host" ]


}
```