#### Parser Content
```Java
{
Name = zoom-z-json-meeting-end-success-ended
  Vendor = Zoom
  Product = Zoom
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"event":"meeting.ended"""" ]
  Fields = [
    """\WdestinationServiceName =({app}.+?)(\s+\w+=|\s*$)""",
    """"end_time"\s*:\s*"({time}\d+-\d+-\d+T\d+:\d+:\d+Z)"""",
    """"event"\s*:\s*"meeting.({operation}ended)"""",
    """"id"\s*:\s*"({meeting_number}\d+)""",
    """"topic"\s*:\s*"({meeting_topic}[^"]+)"""",
    """"type"\s*:\s*({meeting_type}\d)""",
    """"duration"\s*:\s*({meeting_duration}\d+)""",
    """"timezone"\s*:\s*"({meeting_timezone}[^"]+)"""",
    """"host_id"\s*:\s*"({meeting_host_id}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```