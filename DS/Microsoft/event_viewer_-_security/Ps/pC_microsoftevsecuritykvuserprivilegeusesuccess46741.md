#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-user-privilege-use-success-4674-1"
    Vendor = Microsoft
    Product = Event Viewer - Security
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Conditions = ["""EventCode=4674""", """Message=An operation was attempted on a privileged object""", """Logon ID:""", """Object Name:""", """Computer"""]
    Fields = [
      """({event_name}An operation was attempted on a privileged object)""",
      """\s({time}(\d{2}\/){2}\d{4}\s(\d{2}:){2}\d{2}\s(am|AM|pm|PM))\s""",
      """Keywords=Audit\s({action}\w+)\s""",
      """Computer(\w+)?["\s]{0,2000}(:|=)\s*"?({host}[^"\s;]+)""",
      """({event_code}4674)""",
      """Account Name:\s*(LOCAL SERVICE|({user}[^:"]+?))\s+Account Domain:\s*(NT AUTHORITY|({domain}[^":]+?))\s""",
      """"TargetAccount":"(({dest_domain}[^\\\s"]+)\\+)?({dest_user}[^\\\s"]+)""",
      """"SubjectUserSid":"({user_sid}[^\s"]+)""",
      """Logon ID:\s*({login_id}[^\s"]+)""",
      """Object Server:\s*(-|({object_server}[^:"]+?))\s""",
      """Object Name:\s*(-|({object_name}[^:"]+?))\s""",
      """Object Type:\s*(-|({object_type}[^:"]+?))\s""",
      """Process Name:\s*(?: |({process_path}({process_dir}(?:[^";]+)?[\\\/])?({process_name}[^\\\/"\.]+\.\w+?)))"*\s+""",
      """Desired Access:\s*({access}[^:]+?)\s*(?:\s\w+:|$|")""",
      """Privileges:\s*({privileges}[^:"]+?)\s*("|\w+:|$)"""
    ]
    DupFields = ["host->dest_host"]
    ParserVersion = "v1.0.0"


}
```