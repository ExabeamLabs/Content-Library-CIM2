#### Parser Content
```Java
{
Name = microsoft-evsystem-kv-endpoint-password-modify-5823
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a", "dd/MM/yyyy hh:mm:ss a"]
  Conditions = [  """ EventCode=5823 """,""" ComputerName =""" ]
    Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """({event_name}The system successfully changed its password on the domain controller)"""
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