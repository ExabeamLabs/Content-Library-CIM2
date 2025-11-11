#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-delete-success-4734
   Vendor = Microsoft
   Product = Event Viewer - Security
   ParserVersion = "v1.0.0"
   TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
   Conditions = ["""<EventID>4734</EventID>""", """<Provider Name =""", """Microsoft-Windows-Security-Auditing"""]
   Fields = [
     """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
     """<EventID>({event_code}\d+)""",
      """({event_name}A security-enabled local group was deleted)""",
     """<Computer>({dest_host}({host}[^<]+))""",
     """<Execution ProcessID(\\)?=('|")({process_id}\d+)('|") ThreadID(\\)?=('|")({thread_id}\d+)('|")""",
     """<EventRecordID>({event_id}\d+)""",
     """<Data Name(\\)?=('|")TargetSid('|")>({group_id}[^<]+)""",
     """<Data Name(\\)?=('|")TargetUserName('|")>({group_name}[^<]+)""",
     """<Data Name(\\)?=('|")TargetDomainName('|")>({group_domain}[^<]+)""",
     """<Data Name(\\)?=('|")SubjectUserSid('|")>({user_sid}[^<]+)""",
     """<Data Name(\\)?=('|")SubjectUserName('|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
     """<Data Name(\\)?=('|")SubjectDomainName('|")>({src_domain}({domain}[^<]+))""",
     """<Data Name(\\)?=('|")SubjectLogonId('|")>({login_id}[^<]+)""",
     """<Level>({run_level}[^<]+)<"""
   ]
 

}
```