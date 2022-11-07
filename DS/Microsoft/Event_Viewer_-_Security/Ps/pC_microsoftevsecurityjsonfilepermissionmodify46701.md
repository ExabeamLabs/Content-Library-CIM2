#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-permission-modify-4670-1
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [  """EventID":"4670"""", """Permissions on an object were changed""" ]
  Fields =${DLWindowsParsersTemplates.json-windows-system-events.Fields}[
    """"TimeCreated"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Computer"+:"+({host}[^"]+)""""
    """"HandleId":"({object_id}[^"]+)""",
    """"ObjectType":"({object_type}[^"]+)""",
    """"ObjectName":"(?:-|({object_name}[^"]+))""",
    """"NewSd":"({attribute}[^"]+)""",
    """"Category":"({category}[^"]+)""",
    """"Opcode":"({severity}[^"]+)""",
  ]
  DupFields = ["process_name -> file_name"]

json-windows-system-events = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """"EventID"*:"*({event_code}[^,"]+)""",
    """"EventTime"*:"*({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """"Hostname"*:"*({host}[^"]+)"""",
    """"EventType"*:"*({result}[^"]+)""",
    """"Domain"*:"*(-|({domain}[^"]+))""",
    """"Severity"*:"*({severity}[^"]+)"""",
    """"SeverityValue"*:({severity}[^,]+)""",
    """"AccountName"*:"*({user}[^"]+)"""",
    """"SubjectUserSid"*:"*({user_sid}[^"]+)"""",
    """"SubjectUserName"*:"*({user}[^"]+)"""",
    """"SubjectDomainName"*:"*(-|({domain}[^"]+))"""",
    """"LogonID"*:"*({login_id}[^"]+)"""",
    """"ProcessId"*:"*(\\t)*({process_id}[^\\"]+)"""",
    """"ProcessName"*:"*({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
    """"param1"*:"*({process_path}({process_dir}[^,"]*?[\\\/]+)?({process_name}[^\\\/\s"]+?))"""",
    """"TransactionId"*:"*({transaction_id}[^"]+)"""",
    """"Category"*:"*({event_name}[^"]+)""",
    """"Message"*:"*({event_name}[^.]+)""",
  
}
```