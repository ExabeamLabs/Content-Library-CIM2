#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-close-success-562
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [ """EventCode=562""", """Message=Handle Closed""" ]

windows-events-4 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
  Fields = [
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""",
    """"Computer":"({host}[\w\-\.]+)"""",
    """"EventID":({event_code}\d+),""",
    """"Activity":"\d+\s\-\s({event_name}[^"]+)"""",
    """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"IpPort":"({src_port}\d{1,5})"""
  
}
```