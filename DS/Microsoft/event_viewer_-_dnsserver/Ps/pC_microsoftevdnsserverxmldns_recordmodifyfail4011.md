#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-dns_record-modify-fail-4011
  ParserVersion = v1.0.0
  Product = Event Viewer - DNSServer
  Conditions = [ """<EventID>4011</EventID>""", """<Channel>DNS Server</Channel>""", """Microsoft-Windows-DNS-Server-Service""", """<Computer>""" ]
  Fields = ${WindowsParsersTemplates.xml-windows-eventviewer-events.Fields}[
    """<Data Name =('|")User(Context|Name)('|")>(({domain}[^\\\/<]+?)[\\\/]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<""",
    """<Computer>({host}[\w\-\.]+)<"""
    """({provider_name}Microsoft-Windows-DNS-Server-Service)"""
    """({additional_info}The DNS server[^<]+?)\s*<"""
    """<Data Name =('|")param1('|")>({domain}[^\s<]+)"""
    """<Data Name =('|")param2('|")>({dest_network_zone}[^<]+)"""
    """<Data Name =('|")param3('|")>({failure_reason}[^<]+?)\s*<"""
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
	  """<Channel>({channel}[^<]+)<""",
    """<EventRecordID>({event_id}\d+)<\/EventRecordID>"""
	
}
```