#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-network-notification-6004
  ParserVersion = "v1.0.0"
  Product = Event Viewer - DNSServer
  Conditions = [ """>6004</EventID>""","""DNS_EVENT_BAD_ZONE_TRANSFER_REQUEST""", """<Provider>Microsoft-Windows-DNS-Server-Service</Provider>""", """<Channel>DNS Server</Channel>""" ]

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