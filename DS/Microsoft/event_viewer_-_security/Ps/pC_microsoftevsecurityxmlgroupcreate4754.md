#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-create-4754
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """Microsoft-Windows-Security-Auditing""", """<EventID>4754</EventID>""" ]
  Fields = [
    """<Message>({event_name}[^\.:]+?)\.""",
    """<Computer>(::ffff:)?({dest_host}({host}[\w\-.]+))</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)""",
    """<EventID>({event_code}\d+)""",
    """Subject:.+?Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}\S+))\s""",
    """Group:\s*(|-|({group_name}.+?))\s*Security ID:\s*(|-|({group_id}.+?))\s*Group Name:\s*(|-|({=group_name}.+?))\s*Group Domain:\s*(|-|({group_domain}.+?))\s""",
    """Changed Attributes:\s*(|-|(.+?))\s*SAM Account Name:\s*(|-|(.+?))\s*SID History:\s*(|-|({sid_history}.+?))\s*Additional Information:""",
# DL Fields are removed
    """Additional Information:\s*(|-|({additional_info}.+?))\s*Privileges:\s*(|-|({privileges}.+?))\s*($|<)""",
    """EventID="*({event_code}\d+)""",
    """EventType="*({result}[^"\s]+)"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```