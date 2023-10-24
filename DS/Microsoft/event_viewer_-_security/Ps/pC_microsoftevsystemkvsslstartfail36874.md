#### Parser Content
```Java
{
Name = microsoft-evsystem-kv-ssl-start-fail-36874
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a", "dd/MM/yyyy hh:mm:ss a"]
  Conditions = [  """ EventCode=36874 """,""" ComputerName =""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """({event_name}connection request was received from a remote client application)""",
  ]


windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w.-]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<TimeCreated SystemTime\\*='({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\d\d\d\d\d\d\dZ)'""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task}[^<]+)"""
  
}
```