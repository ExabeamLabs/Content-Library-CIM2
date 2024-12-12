#### Parser Content
```Java
{
Name = microsoft-evtaskscheduler-xml-scheduled-task-disable-success-taskdisabled-142
  ParserVersion = v1.0.0
  Product = Event Viewer - TaskScheduler
  Conditions = [ """<EventID>142</EventID>""", """<Channel>Microsoft-Windows-TaskScheduler/Operational</Channel>""", """Microsoft-Windows-TaskScheduler""", """<Computer>""", """TaskDisabled""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-eventviewer-events.Fields}[
    """<Computer>({host}[\w\-\.]+)<"""
    """<Data Name =('|")UserName('|")>({user}[^<]+)<"""
  ]

xml-windows-eventviewer-events = {
	Vendor = Microsoft
	TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
	Fields = [
	  """<EventID>({event_code}\d+)<\/EventID>""",
	  """<Level>({run_level}[^<]+)<""",
	  """SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)""",
	  """<Execution ProcessID=('|")({process_id}\d+)""",
	  """<Security UserID=('|")({user_sid}[\w\-]+)('|")/>""",
	  """ThreadID=('|")({thread_id}[^']+)""",
	  """<Keywords>({result}[^<]+)""",
	  """<EventData Name =('|")(Name|({event_name}[^'"<]+))""",
	  """<Data Name =('|")TaskName('|")>({task_name}[^<]+)<""",
	  """<Data Name =('|")User(Context|Name)('|")>((NT AUTHORITY|({domain}[^\\\/<]+?))[\\\/]+)?(System|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
	  """<Channel>({channel}[^<]+)<""",
    """<EventRecordID>({event_id}\d+)<\/EventRecordID>"""
	
}
```