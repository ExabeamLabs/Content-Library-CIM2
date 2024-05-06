#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-endpoint-notification-4653
  Product = Event Viewer - System
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>4653<""", """An IPsec main mode negotiation failed""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events.Fields}[
    """Local Endpoint:.*?Network Address:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*Keying Module Port:\s*({src_port}\d+)""",
    """Remote Endpoint:.*?Network Address:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s*Keying Module Port:\s*({dest_port}\d+)""",
    """Authentication Method:\s*(-|({auth_method}\S.*?))\s*Role:""",
    """Failure Reason:\s*(-|({failure_reason}.+?))\s*State:""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]

s-xml-events = {
  Vendor = Microsoft
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z?)""",
    """<Computer>({host}[\w\-.]+?)<""",
    """<Message>({event_name}[^:<\.]+)""",
    """<Message>({event_name}[^<]+?)\.(\s|<)""",
    """<Message>({additional_info}[^<]+?)\s*<""",
    """<Message>Process ('|")?({process_name}[^\s'"]+)""",
    """<Security UserID(\\)?=('|")({user_sid}[^'"]+)""",
# update_path is removed
    """<Execution ProcessID(\\)?=('|")({process_id}[^'"]+)""",
    """<EventID[^<]*?>({event_code}\d+)""",
    """<Keyword>({result}[^<]+)<""",
    """<Data Name(\\)?=('|")ProcessName('|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>""",
    """<Data Name\\*=('|")TargetProcessName('|")>({dest_process_path}({dest_process_dir}[^<>]*?[\\\/]+)?({dest_process_name}[^<>\\\/]+))</Data>""",
    """<Data Name(\\)?=('|")ProcessId('|")>({process_id}[^<]+?)\s*<""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+""",
    """Task Name:\s*(|-|({task_name}[^:]+?))\s*Task Content:""",
    """Client IP: ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """ThreadID(\\)?=('|")({thread_id}\d+)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```