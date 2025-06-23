#### Parser Content
```Java
{
Name = "crushftp-cf-str-app-notification-success-crushftp"
  Vendor = "CrushFTP"
  Product = "CrushFTP"
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yyyy HH:mm:ss.SSS"
  Conditions = [ """ CrushFTP.log:""" ]
  Fields = [
    """CrushFTP.log:[^\|]+\|({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\.\d{3})\|"""
	  """({host}[\w\-\.]+)\sCrushFTP.log""",
	  """CrushFTP.log:([^\|]+\|){2}((({event_name}[^:\[\{]+):|({=event_name}[^\|]+)\|))?({additional_info}[^$]+?)\s*$"""
  ]


}
```