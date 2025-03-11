#### Parser Content
```Java
{
Name = microsoft-evsystem-str-policy-apply-processsuccess
  Vendor = Microsoft
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd HH:mm:ss", "EEE MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """The Group Policy settings for the user were processed successfully"""]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})(\s({host}[\w\-.]+)\s)?""",
    """({time}\w{3}\s\w\w\w\s\d\d\s\d\d:\d\d:\d\d\s\d\d\d\d)\s+\d+\s+""",
    """"Computer":"({host}[\w\-\.]+)""""
    """({event_code}1503)"""
    """({event_name}The Group Policy settings for the user were processed successfully)"""
  ]


}
```