#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-file-read-success-4663-4
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "MMM dd HH:mm:ss yyyy"
	ParserVersion = "v1.0.0"
    Conditions = ["""An attempt was made to access an object.""", """"Account":"""]
    Fields = [
      """({event_name}An attempt was made to access an object)""",
      """({host}[\w\-.]+)\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))""",
      """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
      """(?i)(((audit|success)( |_)(success|audit))|information)[\s,]({host}[\w\-.]+).*Subject:""",
      """({event_code}4663)""",
      """"AccessMask":"({access_mask}[^"]+)""",
      """"AccessList":"({access}[^"]+?)\s*"""",
      """"Account":"(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
      """"SubjectUserSid":"({user_sid}[^\s"]+)""",
      """"SubjectLogonId":"({login_id}[^\s"]+)""",
      """"ObjectName":"(-|({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;]+?))?)))\s*"""",
      """"ObjectType":"(-|({file_type}[^\s"]+))""",
      """"ProcessName":"(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/";]+?)))\s*"""",
    ]
  

}
```