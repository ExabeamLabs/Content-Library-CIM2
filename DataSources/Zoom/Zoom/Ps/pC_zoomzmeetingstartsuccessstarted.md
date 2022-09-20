#### Parser Content
```Java
{
Name = zoom-z-meeting-start-success-started
  Vendor = Zoom
  Product = Zoom
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"event":"meeting.started"""" ]
  Fields = [
    """\WdestinationServiceName =({app}.+?)(\s+\w+=|\s*$)""",
    """"start_time"\s*:\s*({time}\d+-\d+-\d+T\d+:\d+:\d+Z)"""",
    """"event"\s*:\s*"meeting.({operation}started)"""",
    """"id"\s*:\s*"({meeting_number}\d+)"""",
    """"topic"\s*:\s*"({meeting_topic}[^"]+)"""",
    """"type"\s*:\s*({meeting_type}\d)""",
    """"host_id"\s*:\s*"({meeting_host_id}[^"]+)"""",
    """"timezone"\s*:\s*"({meeting_timezone}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```