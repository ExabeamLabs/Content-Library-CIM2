#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-driver-load-fail-6281
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>6281<""", """Microsoft-Windows-Security-Auditing""", """<Data Name""","""param1""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """<Computer>({src_host}[^<>]+)<\/Computer>""",
    """({event_code}6281)""",
    """ProcessID\\*=('|")({process_id}\d+)""",
    """ThreadID\\*=('|")({thread_id}\d+)""",
    """<Keywords>({result}[^<]+)<""",
    """<Data Name\\*=('|")param1'>({additional_info}[^<]+)<""",
    """Guid=('|")({process_guid}.+?)('|")"""
    """<Data Name\\*=('|")param1('|")>({file_path}[^<]+)</Data>""",
    """<Data Name\\*=('|")param1('|")>[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)</Data>""",
    """<Data Name\\*=('|")param1('|")>({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)</Data>""",
    """<Level>({run_level}[^<]+)<"""
  ]


}
```