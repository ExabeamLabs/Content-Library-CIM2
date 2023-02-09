#### Parser Content
```Java
{
Name = zoom-z-json-meeting-member-join-success-participant
  Vendor = Zoom
  Product = Zoom
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"event":"meeting.participant""" ]
  Fields = [
    """\WdestinationServiceName =({app}.+?)(\s+\w+=|\s*$)""",
    """"join_time"\s*:\s*"({time}\d+-\d+-\d+T\d+:\d+:\d+Z)"""",
    """"event"\s*:\s*"meeting.({operation}[^"]+)"""",
    """"id"\s*:\s*"({meeting_number}\d+)"""",
    """"topic"\s*:\s*"({meeting_topic}[^"]+)"""",
    """"type"\s*:\s*({meeting_type}\d)""",
    """"host_id"\s*:\s*"({meeting_host_id}[^"]+)"""",
    """"user_name"\s*:\s*"({participant_name}[^"]+)"""",
    """"participant":\{[^\}]*"id":"({participant_id}[^"]+)"""",
    """"timezone"\s*:\s*"({meeting_timezone}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```