#### Parser Content
```Java
{
Name = "microsoft-evsecurity-mix-user-privilege-assign-success-4673"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["MMM dd HH:mm:ss yyyy", "yyyy-MM-dd'T'HH:mm:ss", "MM/dd/yyyy hh:mm:ss a","yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"]
Conditions = [ """A privileged service was called""", """Privileges""", """Account Name:""" ]
Fields = [
  """<EventID>({event_code}\d+)<\/EventID>""",
  """<TimeCreated SystemTime="({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}.\d{1,9}Z)"\/>"""",
  """<Computer>({host}[\w\-\.]+)<\/Computer>""",
  """<EventData><Data>({additional_info}[^\<]+)<\/Data><\/EventData>""",
  """"\@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)""""
  """({time}\d\d\/\d\d\/\d\d\d\d\s+\d\d:\d\d:\d\d\s+(AM|PM))"""
  """TimeGenerated=({time}\d{10})"""
  """"TimeCreated":"[\\\/]*Date\(({time}\d{13})"""
  """"TimeCreated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """({event_name}A privileged service was called)""",
  """"hostname":"({dest_host}[\w\-\.]+)""""
  """<\d+>\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?({dest_host}({host}[\w\-.]+))\s""",
  """<\d+>\w+\s*\d+\s*\d+:\d+:\d+\s+(am\s+|pm\s+)?(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\-.]+))\s""",
  """({time}\w+\s+\d+\s+\d+:\d+:\d+\s+\d+)\s+4673""",
  """\w+\s*\d+\s*\d+:\d+:\d+\s+(::ffff:)?(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|(am|pm|\d{4}|({dest_host}[\w\-.]+)))\s""",
  """:\d{2}\s+({host}[\w.-]+)\s+((audit|success|failure)( |_)(success|audit|failure))\s+4673""",
  """({result}(((audit|success|failure)( |_)(success|audit|failure))|information))\s*(\s|\t|,|#\d+|<[^>]+>)\s*(4673|({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-\.]+))))\s*(\s|\t|,|#\d+|<[^>]+>)\s*""",
  """({event_code}4673)""",
  """"(Hostname|MachineName|computer_name)":"({host}[\w\-.]*)"""
  """Computer(Name)?\s*(=|:)\s*({host}[\w\-.]+)"""
  """Process Name:\s*((?-i)\\+[rnt])*(?: |(\\r|\\t|\\n)|({process_path}({process_dir}(?:[^";]+?)?[\\\/])?({process_name}[^\\\/";]+?)))[\\n\s;]*(Service Request Information:|\w+=)""",
  """Account Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\[srnt])*\s*(Account Domain:|\w+=)""",
  """Account Domain:\s*((?-i)\\+[rnt])*({domain}[^:=]+?)((?-i)\\+[rnt])*\s*(Logon ID:|\w+=)""",
  """Logon ID:\s*((?-i)\\+[rnt])*({login_id}[^:=]+?)\s*((?-i)\\+[rnt])*Service:""",
  """Server:\s*((?-i)\\+[rnt])*({object_server}[^:]+?)\s*((?-i)\\+[rnt])*Service Name:""",
  """Privileges:\s*((?-i)\\+[rnt])*({privileges}[^$]+?)(\s*$|\s+\d+|\\?"|,|;|\s*(xml=)?<)""",
  """Service Name:\s*(-|({service_name}[^\\\s]+?))\s*\w+:"""
  """Channel"?(:|>)"?({channel}[^"<]+)"""
]
ParserVersion = "v1.0.0"


}
```