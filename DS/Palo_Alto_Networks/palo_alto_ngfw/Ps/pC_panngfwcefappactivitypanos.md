#### Parser Content
```Java
{
Name = pan-ngfw-cef-app-activity-panos
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = "MMM dd yyyy HH:mm:ss a"
  Conditions = [ """CEF:""", """Palo Alto Networks|""", """|PAN-OS|""", """|SYSTEM|""" ]
  Fields = [
    """\Wrt=({time}\w+\s+\d+\s+\d+\s+\d+:\d+:\d+\s+\w+)""",
    """\Wrt=({time}\d{13})""",
    """\Wdvchost=({host}[\w\-.]+)""",
# device_external_id is removed
# module is removed
    """\Wmsg="?({event_name}[^"]+?)"?\s+(\w+=|$)""",
    """\WexternalId=({external_id}.+?)\s+(\w+=|$)""",
  ]
  ParserVersion = v1.0.0


}
```