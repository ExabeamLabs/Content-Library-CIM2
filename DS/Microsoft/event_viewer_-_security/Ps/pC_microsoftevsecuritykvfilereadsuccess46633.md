#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-file-read-success-4663-3
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "MMM dd HH:mm:ss yyyy"
	ParserVersion = "v1.0.0"
    Conditions = ["""An attempt was made to access an object.""". """Account Name ="""]
    Fields = [
      """({event_name}An attempt was made to access an object)""",
      """({host}[\w\-.]+)\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))""",
      """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
      """(?i)(((audit|success)( |_)(success|audit))|information)[\s,]({host}[\w\-.]+).*Subject:""",
      """({event_code}4663)""",
      """Subject=.*?Security ID=\s*({user_sid}.+?)[\s;]*Account Name =\s*({user}[\w\.\-]{1,40}\$?)[\s;]*Account Domain=\s*(NT AUTHORITY|({domain}.+?))[\s;]*Logon ID=\s*({login_id}[^\s;]+)[\s;]*Object""",
      """Object=.*?Object Type=\s*({file_type}.+?)[\s;]*Object Name =\s*({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;\\]+?))?))[\s;]*Handle ID(:|=)""",
      """Process Name =\s*(?:|({process_path}.+?))[\s;]*Access Request Information""",
      """Process Name =.*\\({process_name}[^\\;]+?)[\s;]*Access Request Information""",
      """Process Name =\s*(?:|({process_path}({process_dir}(\w:)?(?:[^:;]+)?[\\\/])?({process_name}[^\\\/";]+?)))[\s;]*Access Request Information""",
      """access=\s*({access}.+?)[\s;]*Access Mask=\s*({access_mask}\w+)""",
      """"AccessList":"({access}[^"]+?)\s*"""",
      """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[^\\\s"]+)""",
      """"SubjectUserSid":"({user_sid}[^\s"]+)""",
      """"SubjectLogonId":"({login_id}[^\s"]+)""",
      """"ObjectName":"(-|({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;]+?))?)))\s*"""",
      """"ObjectType":"(-|({file_type}[^\s"]+))""",
      """"ProcessName":"(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*"""",
    ]
    DupFields = ["host->dest_host"]
  

}
```