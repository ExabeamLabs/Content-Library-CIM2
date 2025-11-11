#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-copy-attempttoduplicateobj
  ParserVersion = v1.0.0
  Product = Event Viewer - Security
  Conditions = [ """An attempt was made to duplicate a handle to an object""" ]
  Fields = ${WindowsParsersTemplates.windows-events.Fields}[
    """User=(NOT_TRANSLATED|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(\w+=|$)""",
    """(Primary)? User Name\s*:\s*(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(Primary)? Domain\s*:\s*(-|({domain}[^\s]+))\s""",
    """Caller User Name\s*:\s*(-|({src_user}.+?))\s+Caller Domain\s*:\s*(-|({src_domain}.+?))\s+Caller Logon ID\s*:\s*(-|({login_id}[^\s]+))""",
    """Source Network Address\s*:\s*(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+Source Port:""",
    """ComputerName =({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[\w\-.]+))""",
    """Workstation Name\s*:\s*(-|({src_host_windows}[^\s]+))\s+Logon GUID:""",
    """Workstation Name\s*:\s*(-|({src_host}[\w\-\.]+))\s+Logon GUID:.*?Source Network Address:\s*-\s+""",
# src_handle_id is removed
    """Source Process ID:\s*({src_process_id}[^\s]+)\s+New Handle Information:""",
# target_handle_id is removed
    """Target Process ID:\s*({dest_process_id}[^\s<]+)""",
    """({event_name}An attempt was made to duplicate a handle to an object)""",
    """Logon ID:\s*({login_id}[^\s]+)""",
    """Account Domain:\s*({domain}[^\s]+)""",
    """Account Name:\s*({src_host}[^\s]+)""",
    """Security ID:\s*({user_sid}[^\s]+)"""
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