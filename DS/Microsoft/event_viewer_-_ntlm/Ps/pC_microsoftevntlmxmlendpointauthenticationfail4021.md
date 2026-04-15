#### Parser Content
```Java
{
Name = "microsoft-evntlm-xml-endpoint-authentication-fail-4021"
  Vendor = "Microsoft"
  Product = "Event Viewer - NTLM"
  Conditions = [ """<EventID>4021<""", """<Provider Name =""", """<Channel>Microsoft-Windows-NTLM/Operational</Channel>""" , """NtlmUsageReason"""]
  Fields = ${WindowsParsersTemplates.s-xml-windows-member.Fields}[
    """<Computer>({host}[\w\-.]+)<\/Computer>"""
    """<Data Name =('|")ProcessName('|")>({process_name}[^<]+)</Data>""",
    """<Data Name =('|")ProcessName('|")>({process_path}({process_dir}[^<\/]+?)\\+({process_name}[^<\\]+))<"""
    """<Data Name =('|")ProcessPID('|")>({process_id}[^<]+)</Data>""",
    """<Data Name =('|")Username('|")>({user}[\w\.\-\!\#\^\~]{1,40}\$?)</Data>""",
    """<Data Name =('|")DomainName('|")>({domain}[^<]+)</Data>""",
    """<Data Name =('|")Hostname('|")>({host}[\w\-.]+)</Data>""",
    """<Data Name =('|")NtlmVersion('|")>({version}[^<]+)</Data>"""
  ]
  ParserVersion = "v1.0.0"

s-xml-windows-member = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)""",
    """<EventID>({event_code}[^<]+)</EventID>""",
    """<Data Name(\\)?=('|")MemberName('|")>({user_dn}(cn)=({member}.+?),({user_ou}OU.+?DC=[\w-]+))</Data>""",
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