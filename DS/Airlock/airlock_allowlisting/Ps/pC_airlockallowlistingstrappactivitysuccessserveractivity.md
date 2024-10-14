#### Parser Content
```Java
{
Name = airlock-allowlisting-str-app-activity-success-serveractivity
  ParserVersion = v1.0.0
  Vendor = Airlock
  Product = Airlock Allowlisting
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """ airlock """, """Airlock[""", """]: ServerActivityMessage|""" ]
  Fields = [
    """ServerActivityMessage\|({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s\w{2})\|""",
    """ServerActivityMessage\|[^\|]*\|({operation}[^\|]+)\|""",
    """ServerActivityMessage\|([^\|]*\|){2}(SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\|""",
    """ServerActivityMessage\|([^\|]*\|){3}({additional_info}[^\|$]+?)\s*$""",
    """({event_name}ServerActivityMessage)""",
    """({app}Airlock)"""
  ]


}
```