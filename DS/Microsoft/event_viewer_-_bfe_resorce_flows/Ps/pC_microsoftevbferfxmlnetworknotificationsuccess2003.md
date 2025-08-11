#### Parser Content
```Java
{
Name = microsoft-evbferf-xml-network-notification-success-2003
  Vendor = Microsoft
  Product = Event Viewer - BFE Resorce Flows
  ParserVersion = v1.0.0
  Conditions = [ """<EventID>2003</EventID>""","""<Data Name""","""'ConnectionUsedId'>""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-object-access.Fields}[
    """<Computer>({host}[\w\.\-]+)<""",
    """<Data Name\\*='Protocol'>({protocol}[^<]+)""",
    """<Data Name\\*='ConnectionUsedId'>({connection_id}[^<]+)""",
    """<Data Name\\*='LocalIPAddress'>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Data Name\\*='RemotePort'>({dest_port}\d+)""",
    """<Data Name\\*='RemoteIPAddress'>({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """<Data Name\\*='RemotePort'>({dest_port}\d+)""",
    """<System>.*?Guid='\{({process_guid}[^}]+)""",
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