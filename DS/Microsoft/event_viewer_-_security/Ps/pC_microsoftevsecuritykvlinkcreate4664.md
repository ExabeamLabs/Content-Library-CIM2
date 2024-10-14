#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-link-create-4664
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [  """SourceName =Microsoft Windows security auditing""", """ EventCode=4664 """, """ ComputerName =""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """Account Name:\s*(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|({domain}[^\s]+))\s+Logon ID:""",
    """File Name: (|({file_path}({file_dir}[^"<]*?)[\\\/]*({file_name}[^\\\/"<]+?(\.({file_ext}[^\\\/\.\s"<]+))?))) Link Name:"""
  ]

windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```