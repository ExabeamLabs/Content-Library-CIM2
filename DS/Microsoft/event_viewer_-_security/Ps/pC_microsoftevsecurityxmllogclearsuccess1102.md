#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-log-clear-success-1102"
ParserVersion = "v1.0.0"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
Conditions = ["""The audit log was cleared""", """<EventID>1102""","""<Channel>Security</Channel>""" ]
Fields = [
  """EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
  """Hostname":"({host}[\w\-.]+)""""
  """({event_code}1102)"""
  """({event_name}The audit log was cleared)"""
  """<Message>Process ('|")?({process_name}[^\s']+)"""
  """<Security UserID(\\)?=('|")({user_sid}[^'"]+)"""
  """<Execution ProcessID(\\)?=('|")({process_id}[^"']+)"""
  """<EventID[^<]*?>({event_code}\d+)"""
  """<Keyword>(Classic|({result}[^<]+))</Keyword>""",  
  """<Data Name(\\)?=('|")ProcessName('|")>({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+))</Data>"""
  """<Data Name\\*=('|")TargetProcessName('|")>({dest_process_path}({dest_process_dir}[^<>]*?[\\\/]+)?({dest_process_name}[^<>\\\/]+))</Data>"""
  """<Data Name(\\)?=('|")ProcessId('|")>({process_id}[^<]+?)\s*</Data>"""
  """Security ID:\s*({user_sid}\S+)\s+Account Name:"""
  """Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:"""
  """Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:""",
  """Client IP: ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """ThreadID(\\)?=('|")({thread_id}\d+)"""
  """\s+Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Domain"""
  """\s+Domain Name:\s+({domain}[^\s]+)"""
  """\s+Logon ID:\s+({login_id}[^\s]+)"""
  """SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\d\d\d\dZ)"""
  """\s+Logon ID:\s+({login_id}[^<>\s=]+)"""
  """<Computer>({host}[\w\-.]+?)<\/Computer>"""
  """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  """<Computer>(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?|({dest_host}[\w\-.]+))<\/Computer>"""
  """Security ID:\s*({user_sid}[^\s:]+)"""
  """<Level>({run_level}[^<]+)<"""
]


}
```