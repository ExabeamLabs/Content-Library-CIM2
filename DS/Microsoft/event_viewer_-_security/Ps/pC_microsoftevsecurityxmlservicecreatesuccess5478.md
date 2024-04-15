#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-service-create-success-5478"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """<EventID>5478<""", """<Provider Name ='Microsoft-Windows-Security-Auditing'""", """The IPsec Policy Agent service was started""" ]
Fields = [
  """<EventID>({event_code}\d+)"""
  """<TimeCreated SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """<Computer>({host}[^<]+)"""
  """<Keyword>({result}[^<]+)<\/Keyword>"""
  """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>"""
  """<Message>({event_name}[^<]+)<\/Message>"""
  """Message>.*?<Task>({operation}.*?)<\/Task>"""
  """<Provider Name ='Microsoft-Windows-Security-Auditing' Guid='\{({process_guid}[^}]+?)\}"""
  """<Correlation ActivityID='\{({activity_id}[^\}']+)"""
  """<Execution ProcessID='({process_id}[^']+)"""
  """ThreadID='({thread_id}[^']+)"""
  """<Provider>({provider_name}.+?)<\/Provider>"""
  """({service_name}IPsec Policy Agent)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```