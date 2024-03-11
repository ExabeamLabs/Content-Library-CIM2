#### Parser Content
```Java
{
Name = airlock-allowlisting-str-app-activity-success-fileactivity
  ParserVersion = v1.0.0
  Vendor = Airlock
  Product = Airlock Allowlisting
  TimeFormat = "dd/MM/yyyy HH:mm:ss a"
  Conditions = [ """ airlock """, """Airlock[""", """]: FileActivityMessage|""" ]
  Fields = [
    """FileActivityMessage\|({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s\w{2})\|""",
    """FileActivityMessage\|[^\|]*\|({host}[\w\-\.]+)\|""",
    """FileActivityMessage\|([^\|]*\|){2}(SYSTEM|({user}[^\|]+))\|""",
    """FileActivityMessage\|([^\|]*\|){3}({file_dir}[^\|]+)\|""",
    """FileActivityMessage\|([^\|]*\|){4}({file_name}[^\|]+?(\.(\d{1,5}|({file_ext}[^\.\|]+)))?)\|""",
	"""({event_name}FileActivityMessage)""",
    """({app}Airlock)""",
    """FileActivityMessage\|([^\|]*\|){11}({operation}[^\|]+)\|""",
    """FileActivityMessage\|([^\|]*\|){12}(System|({process_name}[^\|]+))\|"""
  ]


}
```