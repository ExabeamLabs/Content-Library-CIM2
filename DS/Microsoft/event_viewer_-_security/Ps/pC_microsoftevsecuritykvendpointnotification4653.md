#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-4653
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  Conditions = [  """ EventCode=4653 """,""" ComputerName =""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """ComputerName =({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))""",
    """Workstation Name\s*:\s*(-|({src_host_windows}[^\s]+))\s+Logon GUID:""",
    """Workstation Name\s*:\s*(-|({src_host}[\w\-\.]+))\s+Logon GUID:.*?Source Network Address:\s*-\s+""",
    """Local Endpoint:.*?Network Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*Keying Module Port:\s*({src_port}\d+)""",
    """Remote Endpoint:.*?Network Address:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*Keying Module Port:\s*({dest_port}\d+)""",
    """Authentication Method:\s*(-|({auth_method}\S.*?))\s*Role:""",
    """Failure Reason:\s*(-|({failure_reason}.+?))\s*State:"""
  ]

windows-events = {
  Vendor = Microsoft
  Product = Windows
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)('|")""",
    """<EventID>({event_code}\d+)<\/EventID>""",
    """<Message>({event_name}[^<\.]+)""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<Task>({task_name}[^<]+)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```