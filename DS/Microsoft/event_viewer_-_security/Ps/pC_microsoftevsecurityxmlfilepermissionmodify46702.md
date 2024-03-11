#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-file-permission-modify-4670-2
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """<EventID>4670</EventID>""", """<Data Name ='SubjectUserName'>""" ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<Data Name ='ObjectServer'>(-|({object_server}[^<]+))</Data>""",
    """<Data Name ='ObjectType'>(-|({object_type}[^<]+))</Data>""",
    """<Data Name ='ObjectName'>(-|({object_name}[^<]+))</Data>""",
    """<Data Name ='ProcessId'>(-|({process_id}[^<]+))</Data>""",
    """<Data Name ='SubjectUserSid'>(-|({user_sid}[^<]+))</Data>""",
    """<Data Name ='SubjectUserName'>(-|({user}[^<]+))</Data>""",
    """<Data Name ='SubjectDomainName'>(-|({domain}[^<]+))</Data>""",
    """<Data Name ='SubjectLogonId'>(-|({login_id}[^<]+))</Data>""",
    """<Data Name ='ProcessName'>(-|({process_path}(({process_dir}[^<>]+?)[\\\/]+)?({process_name}[^\\\/<>]+?)))</Data>"""
  ]
  DupFields = ["process_name -> file_name"]


}
```