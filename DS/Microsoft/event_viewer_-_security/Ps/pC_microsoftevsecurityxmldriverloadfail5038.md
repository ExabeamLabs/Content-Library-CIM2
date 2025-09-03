#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-driver-load-fail-5038
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
  Conditions = [ """>5038</EventID>""", """Microsoft-Windows-Security-Auditing""", """param1""" ]
  Fields = [
    """({event_name}Code integrity determined that the image hash of a file is not valid)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<(Computer|Hostname)>({src_host}[^<>]+)<\/(Computer|Hostname)>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """SystemTime='?({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
    """<EventTime>({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)<""",
    """({event_code}5038)""",
    """ProcessID\\*=('|")({process_id}\d+)('|")""",
    """ThreadID\\*=('|")({thread_id}\d+)('|")""",
    """({result}AUDIT_FAILURE)<""",
    """<Keyword>({result}[^<]+)<""",
    """<Data Name\\*=('|")param1('|")>({additional_info}[^<]+)<""",
    """Guid='({process_guid}.+?)'"""
    """<ProviderGuid>({process_guid}[^<]+)<"""
    """<Data Name\\*=('|")param1('|")>({file_path}[^<]+)</Data>""",
    """<Data Name\\*=('|")param1('|")>[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)</Data>""",
    """<Data Name\\*=('|")param1('|")>({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)</Data>""",
    """<param1>(-|({file_path}({file_dir}.+?)[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?))|[^\\:<]+)<"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```