#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-service-create-success-5478
  ParserVersion = v1.0.0
  Conditions = [ """destinationServiceName =Azure""", """"Activity":"5478""", """IPsec Services has started successfully."""", """"EventID":5478""", """"EventSourceName":"Microsoft-Windows-Security-Auditing""""]
  Fields = ${WindowsParsersTemplates.json-windows-events-4.Fields}[
    """"ManagementGroupName":"({group_name}[^\s"]+)""",
    """({service_name}IPsec Services)""",
  ]

json-windows-events-4 = {
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
    """"IpAddress":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"IpPort":"({src_port}\d{1,5})"""
  
}
```