#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-group-modify-success-4760
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  Conditions = [ """<EventID>4760</EventID>""", """<Message>A security-disabled universal group was changed""", """Execution ProcessID""" , """<Channel>Security</Channel>""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-object-access.Fields}[
    """<Computer>({host}[\w\.\-]+)<""",
    """Provider Name\\*=('|")({provider_name}[^\'"]+)""",
    """Guid\\*='\{({process_guid}[^\'\}]+)""",
# src_handle_id is removed
    """Source Process ID:\s*({src_process_id}[^\s]+)\s+New Handle Information:""",
# target_handle_id is removed
    """Target Process ID:\s*({dest_process_id}[^\s<]+)""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]

s-xml-object-access = {
  Vendor = Microsoft
  TimeFormat = [ "yyyy-MM-dd'T'HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ" ]
  Fields = [
    """<Message>({event_name}.+?)\s*\.(\s|</Message>)""",
    """<Message>({event_name}.+?)\s+Subject:""",
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)""",
    """>({event_code}[^<]+)</EventID>"""
    """<Channel>({channel}[^<]+)<"""
    """Provider Name\\*=('|")({provider_name}[^\'"]+)"""
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Correlation ActivityID\\*=('|")\{({activity_id}[^\}'"]+)""",
    """<Execution ProcessID\\*=('|")({process_id}[^'"]+)""",
    """ProcessID\\*=('|")({process_id}\d+)""",
    """ThreadID\\*=('|")({thread_id}[^'"]+)""",
    """ActivityID=('|")\{?({activity_id}[^\}'"]+)""",
    """<Keywords?>({result}[^<]+)<\/Keywords?>""",
    """<Provider>({provider_name}.+?)</Provider>""",
    """<Data Name\\*=('|")ErrorCode('|")>({error_code}[^<]+?)\s*<\/Data>""",
    """<Data Name\\*=('|")ErrorDescription('|")>({failure_reason}[^<]+?)\s*</Data>""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*(LOCAL SERVICE|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|({domain}\S+))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+""",
    """Provider Name:\s*({provider_name}.+?)\s+Algorithm Name:""",
# algorithm_name is removed
    """Key Name:\s*({key_name}.+?)\s+Key Type:""",
    """<Data Name =("|')KeyType("|')>({key_type}[^<\.]+)""",
    """Key Type:\s*({key_type}.+?)\.?\s+(Key File Operation Information|Additional Information|Cryptographic Operation)""",
    """File Path:\s*({file_path}.+?)\s+Operation:""",
    """Operation:\s*({operation}[^:]+?)\s+Return Code:""",
    """Return Code:\s*({return_code}.+?)<\/Message>""",
    """Group:\s*(|-|({group_name}.+?))\s*Security ID:\s*(|-|({group_id}.+?))\s*Group Name:((?-i)\\+[rnt])*\s*(|-|({=group_name}.+?))((?-i)\\+[rnt])*\s*Group Domain:\s*(|-|({group_domain}.+?))\s""",
    """<Data Name\\*=('|")RuleId('|")>\{?({rule_id}[^}<]+)""",
    """<Data Name\\*=('|")RuleName('|")>({rule}[^<]+)""",
    """<Level>({run_level}[^<]+)<"""
    """<\/Data><Data Name =('|")MemberSid('|")>(({dest_user_sid}S-\d+-[^<]+)|({account_id}[^<]+))<"""
  
}
```