#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-share-access-5145
    Vendor = Microsoft
    Product = Event Viewer - Security
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """<EventID>5145</EventID>""", """A network share object was checked to see whether client can be granted desired access""", """<Data Name""","""ShareName""" ]
    Fields = [
      """({event_code}5145)""",
      """({event_name}A network share object was checked to see whether client can be granted desired access)""",
      """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """ProcessID\\*=('|")({process_id}\d+)('|")""",
      """<Computer>({host}[^<]+)</Computer>""",
      """<Computer>(\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}|({dest_host}[^<]+)</Computer>)""",
      """<Data Name\\*=('|")SubjectUserSid('|")>({user_sid}[^<]+)</Data>""",
      """<Data Name\\*=('|")SubjectUserName('|")>({user}[^\s<]+)</Data>""",
      """<Data Name\\*=('|")SubjectDomainName('|")>(|NT AUTHORITY|({domain}[^<]+))</Data>""",
      """<Data Name\\*=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
      """<Data Name\\*=('|")ObjectType('|")>({file_type}[^<]+)</Data>""",
      """<Data Name\\*=('|")IpAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """<Data Name\\*=('|")IpPort('|")>({src_port}\d+)""",
      """<Data Name\\*=('|")ShareName('|")>({share_name}[^<]+)</Data>""",
      """<Data Name\\*=('|")RelativeTargetName('|")>({file_dir}[^<]+?\\+)?(?:|({file_name}[^\\:<]*?(\.\s*({file_ext}[^\W_\\.]+?))?))?\?</Data>""",
      """<Data Name\\*=('|")AccessList('|")>\s*({access}[^<]+)\s*</Data>""",
      """<Data Name\\*=('|")AccessReason('|")>\s*(-|({access_reason}[^<]+?))\s*</Data>""",
      """Accesses:[\s]*({access}[^:]*?)\s*Access Check Results:""",
      """<Data Name\\*=('|")ShareLocalPath('|")>(?:[\\\?]+)?(?:\s*|({share_path}(({d_parent}[^<>]+)\\)?({d_name}\s*\S[^\\<>]+?)?)\\?)<\/Data>""",
      """<Keywords><Keyword>({result}[^<]+)</Keyword>"""
      """Source Port(=|:)\s*({src_port}\d+)"""
    ]
  

}
```