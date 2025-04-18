#### Parser Content
```Java
{
Name = cisco-ac-xml-vpn-login-success-2039
  Product = Cisco Remote Access Security
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID Qualifiers='""", """'>2039</EventID>""", """<TimeCreated SystemTime=""", """<Channel>Cisco AnyConnect Secure Mobility Client<""" ]

s-xml-object-access-2 = {
  Vendor = Cisco
  Product = Cisco Remote Access Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """<TimeCreated SystemTime='({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+?)<\/Computer>""",
    """<Message>({event_name}[^.<]+?)\s*<\/Message>""",
    """<Message>({event_name}[^<]+?)\s*\.(\s|<\/Message>)""",
    """<EventID Qualifiers='\d+'>({event_code}\d+)<\/EventID>""",
    """<EventRecordID>({event_id}[^<]+?)<\/EventRecordID>""",
    """<Keywords?>({result}[^<]+)<\/Keywords?>""",
    """<Security UserID='({user_sid}[^']+)""",
    """User SID:\s*({user_sid}[^\s]+)""",
    """User Name:\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """<Execution ProcessID='({process_id}[^']+)""",
    """<Provider>({provider_name}[^<]+?)</Provider>""",
    """ThreadID='({thread_id}[^']+)""",
    """File Name:\s*({file_path}({file_dir}(?:[^<]+)?[\\\/])?({file_name}[^\\\/<]+?(\.({file_ext}[^\\\/\.<\s]+?))))\s+\w+:""",
    """Hash:\s*((&lt;None&gt;)|({file_hash}[^\s]+))""",
  ]
  DupFields = [ "host->dest_host" 
}
```