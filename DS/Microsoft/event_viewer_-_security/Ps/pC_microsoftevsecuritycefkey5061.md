#### Parser Content
```Java
{
Name = microsoft-evsecurity-cef-key-5061
  ParserVersion = "v1.0.0"
  Conditions = [ """"EventID":5061""", """<Data Name""" ]

json-xml-object-access = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Fields = [
    """"Activity":"(\d+\s+-\s+)?({event_name}[^"]+?)"""",
    """"TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Computer":"({host}[^"]+)""",
    """"EventID":"?({event_code}\d+)""",
    """<Data Name[^<>]+?SubjectUserSid[^<>]+?>({user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectUserName[^<>]+?>({user}[\w\.\-]{1,40}\$?)</Data>""",
    """<Data Name[^<>]+?SubjectDomainName[^<>]+?>({domain}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?SubjectLogonId[^<>]+?>({login_id}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?TargetSid[^<>]+?>({dest_user_sid}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?TargetUserName[^<>]+?>(({dest_user}[\w\.\-]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+))<\/Data>""",
    """<Data Name[^<>]+?TargetDomainName[^<>]+?>({dest_domain}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?TargetLogonId[^<>]+?>({dest_login_id}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?ProviderName[^<>]+?>({provider_name}[^<>]+?)</Data>""",
# algorithm_name is removed
    """<Data Name[^<>]+?KeyName[^<>]+?>({key_name}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?KeyType[^<>]+?>({key_type}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?Operation[^<>]+?>({operation}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?ReturnCode[^<>]+?>({return_code}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?KeyFilePath[^<>]+?>({file_path}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?ProcessId[^<>]+?>({process_id}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?ProcessName[^<>]+?>(-|({process_path}({process_dir}[^<>]*?[\\\/]+)?({process_name}[^<>\\\/]+)))</Data>""",
    """<Data Name[^<>]+?KeyName[^<>]+?>({key_name}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?KeyType[^<>]+?>({key_type}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?KeyFilePath[^<>]+?>({file_path}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?Operation[^<>]+?>({operation}[^<>]+?)</Data>""",
    """<Data Name[^<>]+?ReturnCode[^<>]+?>({return_code}[^<>]+?)</Data>""",
    """<Level>({run_level}[^<]+)<"""
  
}
```