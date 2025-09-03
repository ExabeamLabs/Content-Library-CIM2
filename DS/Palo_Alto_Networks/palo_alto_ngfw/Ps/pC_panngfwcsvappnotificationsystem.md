#### Parser Content
```Java
{
Name = pan-ngfw-csv-app-notification-system
  ParserVersion = v1.0.0
  Product = Palo Alto NGFW
  Vendor = Palo Alto Networks
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
  Conditions = [ """,SYSTEM,""", """,0x0""" ]
  Fields = [
      """SYSTEM.+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
      """,({serial_num}({asset_id}\d+)),SYSTEM,""",
      """Deviating device:\s*({device_name}[^,]+)"""
      """({event_category}SYSTEM)""",
      """,SYSTEM,({event_subtype}[^,]+),""",
      """,SYSTEM,([^,]*,){4}({event_code}[^,]+),""",
      """,SYSTEM,([^,]*,){5}\s*(|({object}[^,]+)),""",
      """,SYSTEM,([^,]*,){9}({severity}[^,]+),""",
      """,SYSTEM,(?:[^,]*,){10}"*({event_name}.+?)(?:\.*"|\.\s)""",
      """,SYSTEM,([^,]*,){18}([^,]*,)?({host}[\w\-\.]+)"?$""",
      """,SYSTEM,([^,]*,){18}([^,]*,)?({device_name}({host}[\w\-\.]+))"?$"""
      """:\d\d:\d\d (-|({host}[\w\-\.]+))\s""",
      """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
      """({serial_num}\d+),SYSTEM,"""
      """,SYSTEM,([^,]*,){10}("[^"]+"),([^,]*,){7}({device_name}({host}[^,]+))"""
      """,SYSTEM,([^,]*,){3}({virtual_station_name}[^,]+?)\s*,"""
    ]


}
```