#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-driver-load-fail-5038
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """>5038<""", """Microsoft-Windows-Security-Auditing""", """<Data Name""","""'param1'>""" ]
  Fields = [
    """({event_name}Code integrity determined that the image hash of a file is not valid)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """<Computer>({src_host}[^<>]+)<\/Computer>""",
    """({event_code}5038)""",
    """ProcessID\\*='({process_id}\d+)'""",
    """ThreadID\\*='({thread_id}\d+)'""",
    """<Keyword>({result}[^<]+)<""",
    """<Data Name\\*='param1'>({additional_info}[^<]+)<""",
    """Guid='({process_guid}.+?)'"""
    """<Data Name\\*='param1'>({file_path}[^<]+)</Data>""",
    """<Data Name\\*='param1'>[^<]+[\\\/]+({file_name}(?:[^<\\\/:]+?)(\.({file_ext}\w+))?|[^\\:<]+)</Data>""",
    """<Data Name\\*='param1'>({file_dir}.+?)[\\\/]+(?:[^\\\/]+?)</Data>""",
  ]


}
```