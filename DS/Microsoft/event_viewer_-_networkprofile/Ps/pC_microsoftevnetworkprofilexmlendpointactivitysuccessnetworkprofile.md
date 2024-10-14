#### Parser Content
```Java
{
Name = microsoft-evnetworkprofile-xml-endpoint-activity-success-networkprofile
  ParserVersion = v1.0.0
  Product = Event Viewer - NetworkProfile
  Conditions = [ """Microsoft-Windows-NetworkProfile""", """<Computer>""", """<EventID>""", """<Channel>Microsoft-Windows-NetworkProfile/Operational</Channel>""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-eventviewer-events.Fields}[
    """<Data Name =('|")State('|")>({state}[^<]+)</Data>"""
  ]

xml-windows-eventviewer-events = {
	Vendor = Microsoft
	TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
	Fields = [
	  """<EventID>({event_code}\d+)<\/EventID>""",
	  """<Level>({run_level}[^<]+)<""",
	  """SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{1,9}Z)""",
	  """<Computer>({host}[\w\-\.]+)<""",
	  """<Execution ProcessID=('|")({process_id}\d+)""",
	  """<Security UserID=('|")({user_sid}[\w\-]+)('|")/>""",
	  """ThreadID=('|")({thread_id}[^']+)""",
	  """<Keywords>({result}[^<]+)""",
	  """<EventData Name =('|")(Name|({event_name}[^'"<]+))""",
	  """<Data Name =('|")TaskName('|")>({task_name}[^<]+)<""",
	  """<Data Name =('|")User(Context|Name)('|")>((NT AUTHORITY|({domain}[^\\\/<]+?))[\\\/]+)?(System|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
	  """<Channel>({channel}[^<]+)<"""
	
}
```