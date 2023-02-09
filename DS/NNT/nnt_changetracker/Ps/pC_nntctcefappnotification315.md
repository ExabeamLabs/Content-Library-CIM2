#### Parser Content
```Java
{
Name = nnt-ct-cef-app-notification-315
  ParserVersion = "v1.0.0"
  Conditions = [ """|NNT|ChangeTracker Gen 7|""", """|315|Audit Device Admin|""" ]

nnt-ct-event = {
    Vendor = NNT
    Product = NNT ChangeTracker
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Fields = [
      """rt=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
      """src=({host}[\w\-.]+)\s""",
      """CEF:([^|]*\|){4}({event_code}\d+)""",
      """CEF:([^|]*\|){5}({event_name}[^|]+)""",
      """msg=({additional_info}[^=]+?)\s*(\w+=|$)""",
      """externalId=({external_id}\S+)""",
    
}
```