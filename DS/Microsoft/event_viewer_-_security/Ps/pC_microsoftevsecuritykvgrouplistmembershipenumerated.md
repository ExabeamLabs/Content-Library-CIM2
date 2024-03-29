#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-group-list-membershipenumerated
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MM-dd-yyyy'T'HH:mm:ss.SSS"
  Conditions = [ """A user's local group membership was enumerated""", """Account Name:""" ]
  Fields = [
    """<TimeCreated SystemTime='({time}\d\d-\d\d-\d\d\d\dT\d\d:\d\d:\d\d\.\d{3})""",
    """EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""",
    """({event_code}4798)""",
    """<Computer>({host}.+?)</Computer>""",
    """<Keywords>({result}.+?)</Keywords>""",
    """({event_name}A user's local group membership was enumerated)""",
    """\sSubject:.*?Security ID:\s*(|({user_sid}.+?))\s*Account Name:\s*(|({user}.+?))\s*Account Domain:\s*(|({domain}.+?))\s*Logon ID:\s*(|({login_id}.+?))\s*User:""",
    """\sUser:.*?Security ID:\s*(|({group_id}.+?))\s*(Group|Account) Name:\s*(|({group_name}.+?))\s*(Group|Account) Domain:\s*(|({group_domain}.+?))\s*Process Information:""",
    """Process ID:\s+({process_id}[^\s]+)""",
    """Process Name:\s+(-|({process_path}({process_dir}[^<]*?[\\\/]+)?({process_name}[^\\\/]*?)))\s*(<|$|User:)""",
  ]


}
```