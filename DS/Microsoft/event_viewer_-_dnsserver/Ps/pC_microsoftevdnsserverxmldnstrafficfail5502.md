#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-dns-traffic-fail-5502
  Product = Event Viewer - DNSServer
  ParserVersion = "v1.0.0"
  Conditions = [ """>5502</EventID>""", """DNS_EVENT_BAD_TCP_MESSAGE""", """<Channel>DNS Server</Channel>""" ]
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