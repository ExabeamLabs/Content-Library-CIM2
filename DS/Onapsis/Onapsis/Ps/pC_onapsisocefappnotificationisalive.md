#### Parser Content
```Java
{
Name = onapsis-o-cef-app-notification-isalive
  Product = Onapsis
  Vendor = Onapsis
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|Onapsis|OSP|""", """|Is Alive|""" ]
  Fields = [
    """\Wend=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
# appliance_state is removed
    """\Wevent_id=({event_name}.+?)(\s+\w+=|\s*$)"""
  ]


}
```