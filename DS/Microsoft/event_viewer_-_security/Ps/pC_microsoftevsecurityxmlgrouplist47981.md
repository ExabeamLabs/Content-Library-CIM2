#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-list-4798-1
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Security
  Conditions = [ """<EventID>4798<""", """<Data Name =""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events.Fields}[
    """<Data Name(\\)?=('|")SubjectDomainName('|")>(-|({domain}[^<]+?))<""",
    """Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:""",
    """<Data Name(\\)?=('|")SubjectUserName('|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Client IP: ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Computer>({host}[\w\-.]+?)<""",
    """Status Code:\s*({result}.+?)\s*<""",
    """\sUser:.*?Security ID:\s*(|({group_id}.+?))\s*(Group|Account) Name:\s*(|({group_name}.+?))\s*(Group|Account) Domain:\s*(|({group_domain}.+?))\s*Process Information:""",
    """Process ID:\s+({process_id}[^\s]+)""",
    """Process Name:\s*(-|({process_path}({process_dir}[^=]*?)(\\+({process_name}[^\\]+?))?))("|,|<|$)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Data Name(\\)?=('|")TargetUserName('|")>(-|({dest_user}[^<]+))""",
    """<Data Name(\\)?=('|")TargetDomainName('|")>\s*(-|({dest_domain}[^\s]+?))\s*</Data>""",
    """<Data Name(\\)?=('|")TargetSid('|")>\s*({dest_user_sid}.+?)</Data>\s*""",
    """<Data Name(\\)?=('|")CallerProcessName('|")>({process_path}({process_dir}[^<]*?[\\\/]+)?({process_name}[^<\\\/]+))<\/Data>"""
    """<Data Name(\\)?=('|")CallerProcessId('|")>({process_id}[^<]+)"""
  ]

s-xml-events = {
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{9}Z)"""
    """>({event_code}\d+)</EventID>""",
    """<Security UserID=('|")({user_sid}[^'"]+)('|")\/>""",
    """<Execution ProcessID=('|")({process_id}\d+)('|") ThreadID=('|")({thread_id}\d+)('|")\/>""",
    """<Level>({run_level}[^<]+)<""",
    """<Provider Name =('|")({provider_name}[^'"]+)('|")""",
    """Guid=('|")\{({process_guid}[^\}'"]+?)\}('|")""",
    """<Task>({task_name}[^<]+)""",
    """<Opcode>(0|({opcode}[^<]+))<""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<EventRecordID>({event_id}[^<]+)""",
    """<Channel>({channel}[^<]+)<"""
  
}
```