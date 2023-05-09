#### Parser Content
```Java
{
Name = viscount-i-kv-physical-location-access-cardaccess
  Vendor = Identiv
  Product = Identiv
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [ """, activitytype="""", """, portname="""", """, devicename="""" ]
  Fields = [
    """logtime="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d\d\d)""",
    """info="(Unknown Card|({full_name}[^:]+?))(:|-)\s*({badge_id}\d+)""",
    """devicename="({location_door}[^"]+)""",
    """info=".*?Area:({location_door}[^"]+)""",
    """lastname="(Unknown Card|({last_name}[^"\s]+))""",
    """firstname="({first_name}[^"\s]+)""",
    """cardnumber="({badge_id}\d+)""",
    """result="({result}[^"]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```