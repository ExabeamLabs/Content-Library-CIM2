#### Parser Content
```Java
{
Name = kemp-loadmaster-str-app-notification-disabled
  Vendor = Kemp
  Product = Kemp LoadMaster
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """stats: """, """status:""", """ Total,""", """ Up """, """ Down """, """ Disabled """ ]
  Fields = [
    """stats:\s+({event_name}.+?)\s+$""",
    """({event_category}stats)"""
  ]


}
```