#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-4624
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = ["""An account was successfully logged on""", """Account Name""", """computer_name"""]
    Fields = [
      """({event_name}An account was successfully logged on)""",
      """"(?:winlog\.)?computer_name\\*":\\*"({host}[\w\-.]+)""",
      """({event_code}4624)""",
      """@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """Logon Type(:|=)\s*({login_type}\d+)""",
      """New Logon[\s\S]*?Account Name(:|=)\s*(-|SYSTEM|({user}[\w\.\-\!\#\^\~]{1,40}\$?))[\s;]*Account Domain(:|=)""",
      """New Logon[\s\S]*?Account Domain(:|=)\s*(-|({domain}[^\s]+?))[\s;]*Logon ID(:|=)""",
      """Process Name(:|=)\\*\s*\\*\s*:(?:-|({process_path}({process_dir}.*?)(\\+({process_name}[^\\]+?))?))\s+Network Information:""",
      """Workstation Name(:|=)\s*((?-i)\\+[rnt])*(-|[A-Fa-f:\d.]+|({src_host_windows}[^\\\s;]+))[\s;]*((?-i)\\+[rnt])*Source Network Address(:|=)""",
      """Source Network Address(:|=)\s*(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[\s;]*Source Port(:|=)""",
      """Logon Process(:|=)\s*({auth_process}[^\s;]+)[\s;]*Authentication Package(:|=)\s*({auth_package}[^\s;]+)""",
      """Logon ID(:|=)\s*({login_id}[^\s;]+)[\s;]*(Linked Logon|Logon GUID)""",
      """New Logon(:|=)[\s;]*Security ID(:|=)\s*({user_sid}[^\s;]+)(\s|;)""",
      """EventRecordID>({event_id}[^<]+)<""",
      """SubjectUserName\\?"+:\\?"+(?:-|(?i)(LOCAL SYSTEM|anonymous logon|LOCAL SERVICE|SYSTEM)|({src_user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?""""
      """SubjectDomainName\\?"+:\\?"+(|-|NT Service|NT AUTHORITY|({src_domain}[^"\\]+))\\?""""
      """"ProcessName\\?"+:\\?"+(?:|-|({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/":;\s]+?)))\\?""""
      """IpAddress\\?"+:\\?"(?:-|(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\\?""""
      """ProcessId\\?"+:\\?"+({process_id}[^":\\]+?)\\?""""
      """LogonType\\?"+:\\?"({login_type}\d+)\\?""""
      """SubjectUserSid\\?"+:\\?"+({user_sid}[^"\\]+)\\?""""
      """"LogonProcessName":"({auth_process}[^."]+?)\s*""""
      """AuthenticationPackageName\\?"+:\\?"+({auth_package}[^",\s\\]+)\\?""""
      """SubjectLogonId\\?"+:\\?"+({login_id}[^",\\]+)\\?""""
      """TargetUserName\\?"+:\\?"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\?""""
      """TargetDomainName\\?"+:\\?"({domain}[^\s",\\]+)\\?""""
      """WorkstationName\\?"+:\\?"+(?:-|({src_host_windows}[^",\s\\]+))\\?""""
      """"+mac\\"+:\[\\"+({src_mac}[^\\"]+)"""
    ]
    DupFields = ["host->dest_host","src_host_windows->src_host", "domain->dest_domain", "user->dest_user"]
  

}
```