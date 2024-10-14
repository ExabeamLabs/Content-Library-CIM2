#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-activity-success-eventid
  Product = Event Viewer - Security
  Conditions = [ """<EventID>""", """<Computer>""", """<Provider Name ='Microsoft""" ]

xml-ms-event-viewer = {
    Vendor = Microsoft
    ParserVersion = "v1.0.0"
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
    Fields = [
      """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
      """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
      """Guid\\*=('|")\{({process_guid}[^\'"\}]+)""",
      """<EventRecordID>({event_id}.+?)<""",
      """<Keywords>({result}[^<]+)""",
      """<EventID>({event_code}\d+)""",
      """<Computer>({host}[\w\-.]+)""",
      """<Execution ProcessID\\*=('|")({process_id}\d+)""",
      """<Task>({sub_category}[^<]+)"""
      """<Level>({run_level}[^<]+)<"""
      """<Data Name\\*=('|")ErrorCode('|")>({error_code}\d+)<""",
      """<Data Name =('|")ClientName('|")>({client_name}[^<]+)<""".
      """<Channel>({channel}[^<]+)<"""
    ]
    DupFields = [ "result->result_code" 
}
```