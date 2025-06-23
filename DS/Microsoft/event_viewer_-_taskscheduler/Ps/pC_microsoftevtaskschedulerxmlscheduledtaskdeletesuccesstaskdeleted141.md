#### Parser Content
```Java
{
Name = microsoft-evtaskscheduler-xml-scheduled-task-delete-success-taskdeleted-141
  ParserVersion = v1.0.0
  Product = Event Viewer - TaskScheduler
  Conditions = [ """<EventID>141</EventID>""", """<Channel>Microsoft-Windows-TaskScheduler/Operational</Channel>""", """Microsoft-Windows-TaskScheduler""", """<Computer>""", """TaskDeleted""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-eventviewer-events.Fields}[
    """<Computer>({host}[\w\-\.]+)<"""
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
	  """ThreadID=('|")({thread_id}[^'"]+)""",
	  """<Keywords>({result}[^<]+)""",
	  """<EventData Name =('|")(Name|({event_name}[^'"<]+))""",
	  """<Data Name =('|")TaskName('|")>({task_name}[^<]+)<""",
	  """<Data Name =('|")User(Context|Name)('|")>(({domain}[^\\\/<]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
	  """<Channel>({channel}[^<]+)<""",
    """<EventRecordID>({event_id}\d+)<\/EventRecordID>"""
	
}
```