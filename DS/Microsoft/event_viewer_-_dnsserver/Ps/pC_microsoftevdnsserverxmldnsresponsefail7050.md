#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-dns-response-fail-7050
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - DNSServer
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """>7050</EventID>""","""DNS_EVENT_RECV_CALL_FAILED""", """<Provider>Microsoft-Windows-DNS-Server-Service</Provider>""", """<Channel>DNS Server</Channel>""" ]
  Fields = [
     """<Message>({additional_info}[^<>]+)</Message>""",
     """>({event_code}[^<>]+)</EventID>""",
     """EventData Name ='({event_name}[^>']+)""",
     """<Computer>({host}[^<>]+)</Computer>""",
     """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
     """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
     """<EventRecordID>({event_id}[^<]+)""",
     """<Security UserID\\*='({user_sid}[^']+)""",
     """Guid\\*='\{({process_guid}[^}']+?)\}'""",
     """ProcessID\\*='({process_id}\d+)""",
  ]


}
```