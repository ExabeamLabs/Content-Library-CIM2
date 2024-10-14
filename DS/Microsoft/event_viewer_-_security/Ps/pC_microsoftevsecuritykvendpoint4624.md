#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-4624
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Conditions = [ """,4624,Microsoft-Windows-Security-Auditing""", """Logon Type""", """An account was successfully logged on""" ]
    Fields = [
      """,\w+ ({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d),4624,""",
      """,(Audit Success|Success Audit|Information),({dest_host}[\w\-.]+),""",
      """({event_name}An account was successfully logged on)""",
      """({event_code}4624)""",
      """Logon Type:\s+({login_type}\d+)""",
      """New Logon.*Account Name:\s+(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+(Network )?Account Domain:\s+({domain}[\w.\-]+)""",
      """Process Name:\s+(?:|(?:-|({process_path}({process_dir}.*?)(\\+({process_name}[^\\]+?))?)))\s+Network Information:""",
      """Source Network Address:\s+(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+Source Port:""",
      """Logon Process:\s+({auth_process}[^\s]+)\s+Authentication Package:\s+({auth_package}[^\s]+)""",
      """Logon ID:\s+({login_id}[^\s]+)\s+Logon GUID""",
      """New Logon:\s+Security ID:\s+({user_sid}[^\s]+)\s""",
      """Workstation Name:\s+({src_host_windows}[^\s]+)\s+Source Network"""
      """Key Length:\s*({key_length}\d+)"""
      """\sNetwork Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s]+)"""
    ]
    DupFields = [ "dest_host->host", "src_host_windows->src_host" ]
  

}
```