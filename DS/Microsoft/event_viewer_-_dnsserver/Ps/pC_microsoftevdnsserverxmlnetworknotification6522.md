#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-network-notification-6522
  ParserVersion = "v1.0.0"
  Product = Event Viewer - DNSServer
  Conditions = [ """>6522</EventID>""", """DNS_EVENT_ZONE_TRANSFER_IN_PROGRESS""", """Microsoft-Windows-DNS-Server-Service""", """<Channel>DNS Server</Channel>""" ]
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