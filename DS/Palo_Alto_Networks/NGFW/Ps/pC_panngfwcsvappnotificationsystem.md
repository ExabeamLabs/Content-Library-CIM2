#### Parser Content
```Java
{
Name = pan-ngfw-csv-app-notification-system
  ParserVersion = v1.0.0
  Product = NGFW
  Vendor = Palo Alto Networks
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,SYSTEM,""", """,0x0""" ]
  Fields = [
      """SYSTEM.+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
      """,({host_id}\d+),SYSTEM,""",
      """({event_category}SYSTEM)""",
      """SYSTEM,({event_subtype}[^,]+),""",
      """SYSTEM,([^,]*,){4}({event_code}[^,]+),""",
      """SYSTEM,([^,]*,){5}\s*({object}[^,]+),""",
      """SYSTEM,([^,]*,){9}({severity}[^,]+),""",
      """SYSTEM,(?:[^,]*,){10}"*({event_name}.+?)(?:\.*"|\.\s)""",
      """SYSTEM,([^,]*,){18}([^,]*,)?({host}[\w.-]+)"?$""",
      """:\d\d:\d\d (-|({host}[\w.-]+))\s"""
    ]
  DupFields = ["host->dest_host"]


}
```