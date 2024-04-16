#### Parser Content
```Java
{
Name = nnt-ct-cef-app-notification-911
  ParserVersion = "v1.0.0"
  Conditions = [ """|NNT|ChangeTracker Gen 7|""", """|911|Device Online|""" ]

nnt-ct-event = {
    Vendor = NNT
    Product = NNT ChangeTracker
    TimeFormat = ["MMM dd yyyy HH:mm:ss", "MMM dd HH:mm:ss"]
    Fields = [
      """({time}\w+\s+\d+ \d+:\d+:\d+)"""
      """rt=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
      """src=({host}[\w\-.]+)\s""",
      """CEF:([^|]*\|){4}({event_code}\d+)""",
      """CEF:([^|]*\|){5}({event_name}[^|]+)""",
      """msg=({additional_info}[^=]+?)\s*(\w+=|$)""",
      """externalId=({external_id}\S+)""",
    
}
```