#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-driver-load-fail-5038
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [  """ 5038 """, """ MSWinEventLog """, """Code integrity determined that the image hash of a file is not valid""" ]
  Fields = [
    """ ({time}\w{3} \d\d \d\d:\d\d:\d\d \d\d\d\d)""",
    """:\d+\s({dest_host}({host}[^\s]+))\sMSWinEventLog""",
    """({event_name}Code integrity determined that the image hash of a file is not valid)""",
    """({event_code}5038)""",
    """File Name:\s*({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;\s]+?))?))\s""",
  ]
  ParserVersion = "v1.0.0"


}
```