#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-success-4945
  ParserVersion = "v1.0.0"
  Conditions = [ """EventCode=4945""", """ComputerName =""", """A rule was listed when the Windows Firewall started.""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """ComputerName =({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))""",
    """Workstation Name\s*:\s*(-|({src_host_windows}[^\s]+))\s+Logon GUID:""",
    """Workstation Name\s*:\s*(-|({src_host}[\w\-\.]+))\s+Logon GUID:.*?Source Network Address:\s*-\s+""",
    """RecordNumber=({event_id}\d+)""",
    """TaskCategory=({sub_category}[^=]+)\s+\w+=""",
    """Rule ID:\s*({rule_id}[^\s]+)\s""",
    """Rule Name:\s*({rule}[^:]+)"""
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