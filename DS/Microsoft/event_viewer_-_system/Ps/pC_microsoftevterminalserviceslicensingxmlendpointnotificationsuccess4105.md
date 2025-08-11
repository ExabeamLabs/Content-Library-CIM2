#### Parser Content
```Java
{
Name = microsoft-evterminalserviceslicensing-xml-endpoint-notification-success-4105
  Product = Event Viewer - System
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>4105</EventID>""", """Microsoft-Windows-TerminalServices-Licensing""", """<Security UserID=""","""<Channel>System</Channel>""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events.Fields}[
     """<Computer>({host}[\w\-.]+?)<""",
     """<Provider Name =('|")({provider_name}[^'"]+)('|")""",
     """<param1>({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
     """<param2>({domain}[^<]+)<""",
     """<param3>({error_code}[^<]+)<"""
  ]
  DupFields = ["error_code->failure_code"]

s-xml-events = {
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<Computer>({host}[\w\.\-]+)<""",
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{9}Z)"""
    """>({event_code}\d+)</EventID>""",
    """<Security UserID=('|")({user_sid}[^'"]+)('|")\/>""",
    """<Execution ProcessID=('|")({process_id}\d+)('|") ThreadID=('|")({thread_id}\d+)('|")\/>""",
    """<Level>({run_level}[^<]+)<""",
    """<Provider Name =('|")({provider_name}[^'"]+)('|")""",
    """Guid=('|")\{({process_guid}[^\}'"]+?)\}('|")""",
    """<Task>({task_name}[^<]+)""",
    """<Opcode>(0|({opcode}[^<]+))<""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<EventRecordID>({event_id}[^<]+)""",
    """<Channel>({channel}[^<]+)<"""
  
}
```