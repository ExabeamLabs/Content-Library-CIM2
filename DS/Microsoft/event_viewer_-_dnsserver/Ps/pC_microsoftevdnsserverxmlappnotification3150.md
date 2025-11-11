#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-app-notification-3150
  ParserVersion = "v1.0.0"
  Product = Event Viewer - DNSServer
  Conditions = [ """>3150</EventID>""", """DNS_EVENT_ZONE_WRITE_COMPLETED""", """<Provider>Microsoft-Windows-DNS-Server-Service</Provider>""", """<Channel>DNS Server</Channel>""" ]
  Fields = ${DLWindowsParsersTemplates.windows-events-4.Fields}[
    """<Computer>({host}[^<>]+)</Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]

windows-events-4 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""",
    """"EventID":({event_code}\d+),""",
    """"Activity":"\d+\s\-\s({event_name}[^"]+)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)""""
  
}
```