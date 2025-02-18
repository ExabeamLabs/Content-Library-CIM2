#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-activity-success-eventid
  Product = Event Viewer - Security
  Conditions = [ """<EventID""", """<Computer>""", """<Provider Name ='Microsoft""", """<Channel>Security<""" ]

xml-ms-event-viewer = {
    Vendor = Microsoft
    ParserVersion = "v1.0.0"
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
    Fields = [
      """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
      """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
      """Guid\\*=('|")\{({process_guid}[^\'"\}]+)""",
      """<EventRecordID>({event_id}.+?)<""",
      """<Keywords>({result}[^<]+)""",
      """<EventID>({event_code}\d+)""",
      """<EventID Qualifiers='\d+'>({event_code}\d+)<""",
      """<Data>({additional_info}[^<]+)<""",
      """<Execution ProcessID\\*=('|")({process_id}\d+)""",
      """<Task>({sub_category}[^<]+)"""
      """<Level>({run_level}[^<]+)<"""
      """<Data Name\\*=('|")Error\s*Code('|")>({error_code}[^<]+)<""",
      """<Data Name =('|")ClientName('|")>({client_name}[^<]+)<""".
      """<Channel>({channel}[^<]+)<"""
      """<Computer>({host}[\w\-.]+)"""
    ]
    DupFields = [ "result->result_code" 
}
```