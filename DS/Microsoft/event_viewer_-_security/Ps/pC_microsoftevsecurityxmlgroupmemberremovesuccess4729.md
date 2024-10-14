#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-member-remove-success-4729
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>4729</EventID>""", """TargetSid""", """<Data Name""", """</Data>""" ]
  
s-xml-windows-member = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Computer>({host}[\w\-.]+)<\/Computer>""",
    """<Data Name(\\)?=('|")MemberName('|")>({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>""",
    """<Data Name(\\)?=('|")MemberSid('|")>(({dest_user_sid}S-[^"<]+)|(({account_domain}[^\\<]*)\\)?({account_name}[^<]+))<\/Data>""",
    """<Data Name(\\)?=('|")MemberSid('|")>({dest_user_sid}S-[^\s]+)<\/Data>"""
    """<Data Name(\\)?=('|")TargetUserName('|")>(?=\w)({group_name}[^<]+)</Data>""",
    """<Data Name(\\)?=('|")TargetDomainName('|")>(?=\w)({group_domain}[^<]+)</Data>""",
    """<Data Name(\\)?=('|")TargetSid('|")>({group_id}[^<]+)</Data>""",
    """<Data Name(\\)?=('|")SubjectUserSid('|")>({user_sid}S-[^<]+)</Data>""",
    """<Data Name(\\)?=('|")SubjectUserName('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name(\\)?=('|")SubjectDomainName('|")>({domain}[^<]+)</Data>""",
    """<Data Name(\\)?=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<Data Name(\\)?=('|")RemoteIPAddress('|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name(\\)?=('|")LocalIPAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<""",
    """<Data Name(\\)?=('|")RemotePort('|")>({dest_port}\d+)""",
    """<Data Name(\\)?=('|")LocalPort('|")>({src_port}\d+)""",
    """<Message>({additional_info}[^<]+)""",
    """<Provider>({provider_name}[^<]+)""",
    """<System>.*?Guid(\\)?=('|")\{({process_guid}[^}]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}\d+)""",
    """<Security UserID(\\)?=('|")({user_sid}[^'"]+)""",
    """<Message>({event_name}[^:=<.]+)\."""
    """<Level>({run_level}[^<]+)<"""
  
}
```