#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-policy-modify-5447-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """5447""", """Microsoft-Windows-Security-Auditing""", """<Data Name""","""'FilterName'>""" ]
  Fields = [
    """({event_name}Microsoft-Windows-Security-Auditing)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """({event_code}5447)""",
    """<Data Name\\*='UserName'>(({domain}[^\\]+)\\)?({user}[^<]+)<""",
    """<Data Name\\*='UserSid'>({user_sid}[^<]+)<""",
    """<Data Name\\*='ProcessId'>({process_id}[^<]+)<""",
# change_type is removed
# filter_id is removed
# filter_type is removed
# filter_name is removed
    """<Data Name\\*='LayerName'>({layer_name}[^<]+)<""",
  ]


}
```