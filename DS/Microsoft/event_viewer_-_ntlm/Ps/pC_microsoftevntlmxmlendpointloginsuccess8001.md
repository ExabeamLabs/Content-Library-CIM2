#### Parser Content
```Java
{
Name = microsoft-evntlm-xml-endpoint-login-success-8001
  Vendor = Microsoft
  Product = Event Viewer - NTLM
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Conditions = [ """<EventID>8001<""", """<Message>NTLM client blocked audit: Audit outgoing NTLM authentication traffic that would be blocked""", """<Channel>Microsoft-Windows-NTLM/Operational<""" ]
  Fields = [
    """SystemTime='({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)"""
    """<Computer>({host}[^<]+?)<\/Computer>"""
    """Security UserID='({user_sid}[^'\/>]+)"""
    """({event_code}8001)"""
    """<Data Name ='ClientUserName'>(\((?i)NULL\)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<\/Data>"""
    """<Data Name ='ClientDomainName'>(\((?i)NULL\)|({domain}[^<]+))<"""
    """({event_name}NTLM client blocked)"""
    """<Message>({additional_info}[^<]+)<"""
    """<Data Name ='Workstation'>(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(?:(?!NULL)(Unknown|({src_host}[^\s.]+))(\.[^\s]+)?))<\/Data>"""
    """<Data Name ='LogonType'>({login_type}\d+)<\/Data>"""
    """<Data Name ='ProcessName'>({process_path}({process_dir}[^<\/]+?)\\+({process_name}[^<\\]+))<"""
    """<Level>({run_level}[^<]+)<"""
   ]


}
```