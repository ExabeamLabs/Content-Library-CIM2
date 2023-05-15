#### Parser Content
```Java
{
Name = microfocusarcsight-ma-cef-app-notification-success-arcsight
	  ParserVersion = v1.0.0
    Vendor = MicroFocus ArcSight
    Product = MicroFocus ArcSight
    TimeFormat = "epoch"
    Conditions = ["""CEF:""", """|ArcSight|ArcSight|"""]
    Fields = [
      """\srt=({time}\d{13})""",
      """\sdvchost=({host}[^\s]+)""",
      """CEF:([^|]*\|){5}({event_name}[^|]+)""",
      """eventId=({event_code}[^=]+)\s\w+=""",
      """msg=({additional_info}.+?)\s\w+=""",
      """fname=({file_path}({file_dir}[^=]+)[\\\/]({file_name}[^=]+))\s\w+="""
    ]


}
```