#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-dns-traffic-fail-7050-1
  Product = Event Viewer - DNSServer
  Conditions = [ """<EventID>7050<""", """<Computer>""", """<Provider Name =""", """Microsoft-Windows-DNS-Server-Service""", """<Channel>DNS Server</Channel>""", """DNS_EVENT_RECV_CALL_FAILED""" ]

xml-ms-event-viewer = {
    Vendor = Microsoft
    ParserVersion = "v1.0.0"
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
    Fields = [
      """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
      """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
      """Guid\\*=('|")\{({process_guid}[^\'"\}]+)""",
      """<EventRecordID>({event_id}.+?)<""",
      """<Keywords>({result_code}({result}[^<]+))""",
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
    
}
```