#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-service-create-success-5478
  ParserVersion = v1.0.0
  Conditions = [ """"Activity":"5478""", """IPsec Services has started successfully."""", """"EventID":5478""", """"EventSourceName":"Microsoft-Windows-Security-Auditing""""]
  Fields = ${WindowsParsersTemplates.json-windows-events-4.Fields}[
    """"IpAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"IpPort":"({src_port}\d{1,5})""",
    """"ManagementGroupName":"({group_name}[^\s"]+)""",
    """({service_name}IPsec Services)""",
    """"Computer":"({dest_host}({host}[\w\-\.]+))""""
    """"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """"SubjectDomainName":"({src_domain}({domain}[^"]+))""""
  ]

json-windows-events-4 = {
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