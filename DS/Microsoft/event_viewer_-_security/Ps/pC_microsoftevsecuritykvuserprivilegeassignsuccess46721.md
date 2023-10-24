#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-user-privilege-assign-success-4672-1
   Vendor = Microsoft
   Product = Event Viewer - Security 
   ParserVersion = "v1.0.0"
   TimeFormat = "yyyy-MM-dd HH:mm:ss"
   Conditions = [ """EventID=4672""", """Special privileges assigned to new logon""", """Privileges=""", """ComputerName =""" ]
   Fields = [
      """({event_code}4672)""",
      """({event_name}Special privileges assigned to new logon)""",
      """DetectTime=({time}\d+-\d+-\d+\s\d+:\d+:\d+)""",
      """ComputerName =({host}[\w\-.]+)\s+\w+=""",
      """EventType=({result}\w.+?)\s*\w+=""",
      """Account Name =\s*(-|SYSTEM|({user}[\w\.\-]{1,40}\$?))[\s;]+""",
      """User=(?:(?i)null|({user}[\w\.\-]{1,40}\$?))\s+""",
      """Account Domain=\s*(-|({domain}[^\s\:\=]+?))[\s;]+""",
      """Security ID=\s*(|(({domain}[^\\\s\:\=]+)[\\]({user}[\w\.\-]{1,40}\$?))|({user_sid}[^\s\:\=]+?))\s+""",
      """Privileges=\s*({privileges}.+?)(,|\s*"|;|\s*$)""",
      """Logon ID=\s*({login_id}[^\s\=]+)\s+""",
      """EventSource=({log_source}[^\s\=]+)\s*\w+="""
   ]
    DupFields = ["host->dest_host"]
 

}
```