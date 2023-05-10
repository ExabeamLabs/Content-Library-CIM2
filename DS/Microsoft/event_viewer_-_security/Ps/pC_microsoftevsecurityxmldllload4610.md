#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-dll-load-4610
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """>4610<""", """Microsoft-Windows-Security-Auditing""", """<Data Name ='AuthenticationPackageName'>""" ]
  Fields = [
    """({event_name}An authentication package has been loaded by the Local Security Authority)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({src_host}[^<>]+)<\/Computer>""",
    """({event_code}4610)""",
    """ProcessID='({process_id}\d+)'""",
    """ThreadID='({thread_id}\d+)'""",
    """<Keyword>({result}[^<]+)<""",
    """<Data Name ='AuthenticationPackageName'>({auth_package}[^<]+)<""",
  ]


}
```