#### Parser Content
```Java
{
Name = unix-unix-str-endpoint-activity-success-rgmanager
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """rgmanager[""", """]: [""" ]
  Fields = [
    """\srgmanager\[\d+\]:\s*({additional_info}.+?)\s*$""",
    """\d\d:\d\d:\d\d(\.\S+)?\s({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s*({host}[^\s]+)\srgmanager""",
  ]


}
```