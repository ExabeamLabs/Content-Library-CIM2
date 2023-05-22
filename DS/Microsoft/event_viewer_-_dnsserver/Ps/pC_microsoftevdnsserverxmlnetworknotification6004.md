#### Parser Content
```Java
{
Name = microsoft-evdnsserver-xml-network-notification-6004
  ParserVersion = "v1.0.0"
  Product = Event Viewer - DNSServer
  Conditions = [ """>6004</EventID>""","""DNS_EVENT_BAD_ZONE_TRANSFER_REQUEST""", """<Provider>Microsoft-Windows-DNS-Server-Service</Provider>""", """<Channel>DNS Server</Channel>""" ]

windows-events-4 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""",
    """"Computer":"({host}({dest_host}[\w\-\.]+))"""",
    """"EventID":({event_code}\d+),""",
    """"Activity":"\d+\s\-\s({event_name}[^"]+)"""",
    """"SubjectUserName":"({user}[^"]+)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"IpPort":"({src_port}\d{1,5})"""
  
}
```