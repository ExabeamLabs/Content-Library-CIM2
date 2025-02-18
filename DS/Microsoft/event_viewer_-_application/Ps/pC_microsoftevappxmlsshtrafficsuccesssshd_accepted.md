#### Parser Content
```Java
{
Name = microsoft-evapp-xml-ssh-traffic-success-sshd_accepted
  Vendor = "Microsoft"
  Product = "Event Viewer - Application"
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<Provider Name ='sshd'/>""", """<TimeCreated SystemTime""","""<Channel>Application</Channel>""", """: Accepted """ ]
  Fields = [
    """<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
    """<Computer>({host}({dest_host}[\w\-.]+))<\/Computer>""",
    """\<Security UserID\\?=('|")({user_sid}[^']+)'"""
    """\sPID\s({process_id}\d+):""",
    """\s({additional_info}Accepted \w+ for\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)\sfrom\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\sport\s({src_port}\d+)?\s\S+?)<""",
    """<Keywords>({result}[^<]+)</Keywords>""",
    """({protocol}ssh)""",
    """<EventRecordID>({event_id}\d+)<""",
    """<EventID Qualifiers='0'>({event_code}\d+)</EventID>"""
    """<Level>({run_level}[^<]+)<"""
  ]


}
```