#### Parser Content
```Java
{
Name = datawatchsystems-datawatch-str-physical_location-access-badgeaccess
  ParserVersion = v1.0.0
  Vendor = DataWatch Systems
  Product = DataWatch 
  TimeFormat =  "MM/dd/yy HH:mm:ss"
  Conditions = [ """DataWatch""","""Badge Access""" ]
  Fields = [ 
    """\|({time}\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)\|""",
    """(?:([^\|]*\|)){4}({action}.+?)(:.+?)?\s+At\s+({location_door}[^\|]+)\|""",
    """(?:([^\|]*\|)){5}({last_name}[^,]+),({first_name}[^\|]+)\|""",
    """(?:([^\|]*\|)){6}({badge_id}[^\|]+)\|""",
  ]


}
```