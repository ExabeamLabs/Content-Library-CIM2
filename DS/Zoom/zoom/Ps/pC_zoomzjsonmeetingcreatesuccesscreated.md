#### Parser Content
```Java
{
Name = zoom-z-json-meeting-create-success-created
  Vendor = Zoom
  Product = Zoom
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"event":"meeting.created"""" ]
  Fields = [
    """\WdestinationServiceName =({app}.+?)(\s+\w+=|\s*$)""",
    """\Wend=({time}\d{13})""",
    """"event"\s*:\s*"meeting.({operation}created)"""",
    """"operator"\s*:\s*"({email_address}[^\s@"]+@[^\s@"]+)"""",
    """"operator_id"\s*:\s*"({meeting_host_id}[^"]+)"""",
    """"id"\s*:\s*({meeting_number}\d+)""",
    """"topic"\s*:\s*"({meeting_topic}[^"]+)"""",
    """"type"\s*:\s*({meeting_type}\d)""",
    """"duration"\s*:\s*({meeting_duration}\d+)""",
    """"timezone"\s*:\s*"({meeting_timezone}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```