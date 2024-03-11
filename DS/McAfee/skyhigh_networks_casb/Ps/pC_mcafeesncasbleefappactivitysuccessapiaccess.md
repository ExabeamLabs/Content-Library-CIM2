#### Parser Content
```Java
{
Name = mcafee-sncasb-leef-app-activity-success-apiaccess
    Conditions = [ """|McAfee (Skyhigh)|Dashboard Audit Logs|""", """API Access""" ]
    ParserVersion = "v1.0.0"
  
cef-mcafee-skyhigh-activity = {
    Vendor = McAfee
    Product = Skyhigh Networks CASB
    ParserVersion = "v1.0.0"
    TimeFormat = "MMM dd yyyy HH:mm:ss.SSS z"
    Fields = [
      """\Wcat=(|({result}.+?))(\s+\w+=|\s*$)""",
      """({host}[\w.\-]+)\s+(LEEF|CEF):""",
      """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
      """({app}Skyhigh)""",
      """\W(start|devTime)=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d\.\d+ \w+)""",
      """\W(suser|usrName)=(N\/A|({email_address}[^@=]+?@[^@=]+?)|({user}[^\s]+?))(\s+\w+=|\s*$)""",
      """\Wdescription=(|({additional_info}.+?))(\s+\w+=|\s*$)""",
      """\WobjectName =(|null|({object}.+?))(\s+\w+=|\s*$)""",
      """\WuserInfoEmail=(|({email_address}[^@]+({email_domain}.+?)))(\s+\w+=|\s*$)""",
      """\WuserInfoFirstName =(|({first_name}.+?))(\s+\w+=|\s*$)""",
      """\WuserInfoLastName =(|({last_name}.+?))(\s+\w+=|\s*$)""",
    
}
```