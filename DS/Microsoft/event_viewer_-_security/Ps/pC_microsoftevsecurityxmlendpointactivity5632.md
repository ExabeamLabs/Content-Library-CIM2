#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-activity-5632
  Product = Event Viewer - Security
  Conditions = [ """<Provider Name ="Microsoft-Windows-Security-Auditing"""", """<EventID>5632<""", """<Channel>Security<""" ]
  Fields = ${MSEventViewerTemplates.xml-ms-event-viewer.Fields}[
    """<Computer>({host}[\w\-.]+)"""
  ]

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