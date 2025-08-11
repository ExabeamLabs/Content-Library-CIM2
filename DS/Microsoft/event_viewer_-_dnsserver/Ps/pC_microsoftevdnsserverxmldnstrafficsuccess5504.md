#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-dns-traffic-success-5504
  ParserVersion = v1.0.0
  Product = Event Viewer - DNSServer
  Conditions = [ """<EventID>5504</EventID>""", """<Channel>DNS Server</Channel>""", """Microsoft-Windows-DNS-Server-Service""", """DNS_EVENT_INVALID_PACKET_DOMAIN_NAME""", """<Computer>""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-eventviewer-events.Fields}[
    """<Computer>({host}[\w\-\.]+)<"""
    """<Data Name =('|")param1('|")>(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))</Data>"""
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