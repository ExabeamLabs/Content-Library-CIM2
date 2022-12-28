#### Parser Content
```Java
{
Name = zoom-z-json-meeting-modify-success-updated
  Vendor = Zoom
  Product = Zoom
  TimeFormat = "epoch"
  Conditions = [ """"event":"meeting.updated"""" ]
  Fields = [
    """\WdestinationServiceName =({app}.+?)(\s+\w+=|\s*$)""",
    """"operator"\s*:\s*"({email_address}[^\s@"]+@[^\s@"]+)"""",
    """"operator_id"\s*:\s*"({meeting_host_id}[^"]+)"""",
    """"event"\s*:\s*"meeting.({operation}updated)"""",
    """"old_object"\s*:\s*\{.*?"password"\s*:\s*"({old_password}[^"]+)"""",
    """"object"\s*:\s*\{.*?"password"\s*:\s*"({new_password}[^"]+)"""",
    """"object"\s*:\s*\{"id"\s*:\s*({meeting_number}\d+)""",
    """"time_stamp"\s*:\s*({time}\d{13})"""  
]
  ParserVersion = "v1.0.0"


}
```