#### Parser Content
```Java
{
Name = microsoft-windows-xml-vpn-logout-success-1018
  Product = "Event Viewer - WinNat"
  Conditions = [ """<EventID>1018</EventID>""", """<Data Name""","""TransportProtocol""" , """<Channel>Microsoft-Windows-WinNat""" ]
  Fields = ${WindowsParsersTemplates.s-xml-windows-member.Fields}[
    """<Data Name(\\)?=('|")SubjectUserName('|")>({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))</Data>""",
    """<Data Name(\\)?=('|")SubjectDomainName('|")>({src_domain}({domain}[^<]+))</Data>""",
    """<Data Name(\\)?=('|")RemoteIPAddress('|")>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name(\\)?=('|")LocalIPAddress('|")>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<""",
    """<Data Name(\\)?=('|")RemotePort('|")>({dest_port}\d+)""",
    """<Data Name(\\)?=('|")LocalPort('|")>({src_port}\d+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """<Computer>({host}[\w\-.]+)<\/Computer>"""
  ]
  ParserVersion = "v1.0.0"

s-xml-windows-member = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """<Data Name(\\)?=('|")MemberName('|")>({user_dn}(?i)(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>""",
    """<Data Name(\\)?=('|")MemberSid('|")>(({dest_user_sid}S-[^"<]+)|(({account_domain}[^\\<]*)\\)?({account_name}[^<]+))<\/Data>""",
    """<Data Name(\\)?=('|")MemberSid('|")>({dest_user_sid}S-[^\s]+)<\/Data>"""
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """Guid\\*=('|")\{({process_guid}[^\'\}]+)""",
    """<Task>({task_name}[^<]+)<"""
    """<Opcode>({opcode}[^<]+?)<""",
    """<Keywords>({result}[^<]+)<"""
    """<EventRecordID>({event_id}[^<]+)<"""
    """<Channel>({channel}[^<]+)<""",
    """<Data Name(\\)?=('|")TargetUserName('|")>(?=\w)?({group_name}[^<]+)</Data>""",
    """<Data Name(\\)?=('|")TargetDomainName('|")>(?=\w)({group_domain}[^<]+)</Data>""",
    """<Data Name(\\)?=('|")TargetSid('|")>({group_id}[^<]+)</Data>""",
    """<Data Name(\\)?=('|")SubjectUserSid('|")>({user_sid}S-[^<]+)</Data>""",
    """<Data Name(\\)?=('|")SubjectLogonId('|")>({login_id}[^<]+)</Data>""",
    """<Message>({additional_info}[^<]+)""",
    """<Provider>({provider_name}[^<]+)""",
    """<System>.*?Guid(\\)?=('|")\{({process_guid}[^}]+)""",
    """<Execution ProcessID(\\)?=('|")({process_id}\d+)""",
    """<Security UserID(\\)?=('|")({user_sid}[^'"]+)""",
    """<Message>({event_name}[^:=<.]+)\."""
    """<Level>({run_level}[^<]+)<"""
  
}
```