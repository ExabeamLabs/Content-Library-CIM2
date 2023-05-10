#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-dns-traffic-fail-5502
  Product = Event Viewer - DNSServer
  ParserVersion = "v1.0.0"
  Conditions = [ """>5502</EventID>""", """DNS_EVENT_BAD_TCP_MESSAGE""", """<Channel>DNS Server</Channel>""" ]

windows-events-4 = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
     """<Message>({additional_info}[^<>]+)</Message>""",
     """>({event_code}[^<>]+)</EventID>""",
     """EventData Name ='({event_name}[^>']+)""",
     """<Computer>({host}[^<>]+)</Computer>""",
     """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
     """<EventRecordID>({event_id}[^<]+)""",
     """<Security UserID='({user_sid}[^']+)""",
     """Guid='\{({process_guid}[^}']+?)\}'""",
     """ProcessID='({process_id}\d+)""",
  
}
```