#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-file-success-4663-7
    ParserVersion = v1.0.0
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = ["MMM dd HH:mm:ss yyyy", "MMM dd HH:mm:ss"]
    Conditions = ["An attempt was made to access an object.", "Account Name:"]
    Fields = [
      """({time}\w+\s+\d+ \d+:\d+:\d+)"""
      """({event_name}An attempt was made to access an object)""",
      """({host}[\w\-.]+)\s+({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+\s+(am|AM|pm|PM))""",
      """({time}(?i)(Jan|Feb|Mar|Apr|May|Jun|Jul|Aug|Sep|Oct|Nov|Dec) \d{1,2} \d{1,2}:\d{1,2}:\d{1,2} 20\d{2})""",
      """(?i)(((audit|success)( |_)(success|audit))|information)[\s,]({host}[\w\-.]+)\s.*Subject:""",
      """({event_code}4663)""",
      """Subject:.*?Security ID:\s*({user_sid}.+?)[\s;]*Account Name:\s*({user}[\w\.\-]{1,40}\$?)[\s;]*Account Domain:\s*(NT AUTHORITY|({domain}.+?))[\s;]*Logon ID:\s*({login_id}[^\s;]+)[\s;]*Object""",
      """Object:.*?Object Type:\s*({file_type}.+?)[\s;]*Object Name:\s*({file_path}({file_dir}.*?)({file_name}[^\\\/;]+?(\.({file_ext}[^\.;\\]+?))?))[\s;]*Handle ID""",
      """Process Name:\s*(?:|({process_path}.+?))[\s;]*Access Request Information:""",
      """Process Name:.*\\({process_name}[^\\;]+?)[\s;]*Access Request Information:""",
      """Process Name:\s*(?:|({process_path}({process_dir}(\w:)?(?:[^:;]+)?[\\\/])?({process_name}[^\\\/";]+?)))[\s;]*Access Request Information:""",
      """Accesses:\s*({access}.+?)[\s;]*Access Mask:\s*({access_mask}\w+)""",
    ]
  

}
```