#### Parser Content
```Java
{
Name = microsoft-evpowershell-xml-endpoint-activity-success-eventid
  Product = Event Viewer - PowerShell
  Conditions = [ """<EventID""", """<Computer>""",  """<Provider Name =""", """Microsoft""", """<Channel>Microsoft-Windows-PowerShell""" ]

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
      """<EventID Qualifiers=('|")\d+('|")>({event_code}\d+)<""",
      """<Data>({additional_info}[^<]+)<""",
      """ProcessID\\*=('|")({process_id}\d+)""",
      """<Task>({sub_category}[^<]+)""",
      """<Level>({run_level}[^<]+)<""",
      """('|")Error\s*Code('|")>({error_code}[^<]+)<""",
      """<Data Name =('|")ClientName('|")>({client_name}[^<]+)<""".
      """<Channel>({channel}[^<]+)<""",
      """<Computer>({host}[\w\-.]+)""",
      """<EventData Name =('|")({event_name}[^>'"]+)('|")>""",
      """<Security UserID=('|")({user_sid}[^'"<]+?)('|")"""
    ]
    DupFields = [ "result->result_code" 
}
```