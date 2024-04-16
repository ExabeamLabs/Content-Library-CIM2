#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-success-4945
  ParserVersion = "v1.0.0"
  Conditions = [ """EventCode=4945""", """ComputerName =""", """A rule was listed when the Windows Firewall started.""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """RecordNumber=({event_id}\d+)""",
    """TaskCategory=({sub_category}[^=]+)\s+\w+=""",
    """Rule ID:\s*({rule_id}[^\s]+)\s""",
    """Rule Name:\s*({rule_name}[^:]+)"""
  ]
  
windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```