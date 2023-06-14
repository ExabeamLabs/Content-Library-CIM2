#### Parser Content
```Java
{
Name = microsoft-evapp-xml-endpoint-notification-10
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Application
  Conditions = [ """<EventID>10</EventID>""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-object-access.Fields}[
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]

s-xml-object-access = {
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Fields = [
    """<Message>({event_name}.+?)\s*\.(\s|</Message>)""",
    """<Message>({event_name}.+?)\s+Subject:""",
    """<TimeCreated SystemTime\\*=('|")({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """<Computer>({host}[^<>]+)<\/Computer>""",
    """<EventID>({event_code}[^<]+)<\/EventID>""",
    """<EventRecordID>({event_id}[^<]+)<\/EventRecordID>""",
    """<Correlation ActivityID\\*=('|")\{({activity_id}[^\}'"]+)""",
    """<Execution ProcessID\\*=('|")({process_id}[^'"]+)""",
    """ProcessID\\*=('|")({process_id}\d+)""",
    """ThreadID\\*=('|")({thread_id}[^'"]+)""",
    """ActivityID=('|")\{?({activity_id}[^\}'"]+)""",
    """<Keywords?>({result}[^<]+)<\/Keywords?>""",
    """<Provider>({provider_name}.+?)</Provider>""",
    """<Data Name\\*=('|")ErrorDescription('|")>({failure_reason}[^<]+?)\s*</Data>""",
    """Security ID:\s*({user_sid}\S+)\s+Account Name:""",
    """Account Name:\s*(LOCAL SERVICE|({user}\S+))\s+Account Domain:""",
    """Account Domain:\s*(NT AUTHORITY|({domain}\S+))\s+Logon ID:""",
    """Logon ID:\s*({login_id}\S+)\s+""",
    """Provider Name:\s*({provider_name}.+?)\s+Algorithm Name:""",
# algorithm_name is removed
    """Key Name:\s*({key_name}.+?)\s+Key Type:""",
    """Key Type:\s*({key_type}.+?)\s+(Key File Operation Information|Additional Information|Cryptographic Operation)""",
    """File Path:\s*({file_path}.+?)\s+Operation:""",
    """Operation:\s*({operation}[^:]+?)\s+Return Code:""",
    """Return Code:\s*({return_code}.+?)<\/Message>""",
    """Group:\s*(|-|({group_name}.+?))\s*Security ID:\s*(|-|({group_id}.+?))\s*Group Name:\s*(|-|({=group_name}.+?))\s*Group Domain:\s*(|-|({group_domain}.+?))\s""",
    """<Data Name\\*=('|")RuleId('|")>\{?({rule_id}[^}<]+)""",
    """<Data Name\\*=('|")RuleName('|")>({rule}[^<]+)""",
  
}
```