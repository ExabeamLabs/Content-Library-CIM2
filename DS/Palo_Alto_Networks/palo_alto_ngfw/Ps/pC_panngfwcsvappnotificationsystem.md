#### Parser Content
```Java
{
Name = pan-ngfw-csv-app-notification-system
  ParserVersion = v1.0.0
  Product = Palo Alto NGFW
  Vendor = Palo Alto Networks
  TimeFormat = "yyyy/MM/dd HH:mm:ss"
  Conditions = [ """,SYSTEM,""", """,0x0""" ]
  Fields = [
      """SYSTEM.+?({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d)""",
      """,({asset_id}\d+),SYSTEM,""",
      """({event_category}SYSTEM)""",
      """SYSTEM,({event_subtype}[^,]+),""",
      """SYSTEM,([^,]*,){4}({event_code}[^,]+),""",
      """SYSTEM,([^,]*,){5}\s*({object}[^,]+),""",
      """SYSTEM,([^,]*,){9}({severity}[^,]+),""",
      """SYSTEM,(?:[^,]*,){10}"*({event_name}.+?)(?:\.*"|\.\s)""",
      """SYSTEM,([^,]*,){18}([^,]*,)?({host}(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+)))"?$""",
      """:\d\d:\d\d (-|({host}(({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-\.]+))))\s"""
    ]


}
```