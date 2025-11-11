#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-app-authentication-fail-1203
  ParserVersion = "v1.0.0"
  Product = Event Viewer - Security
  Conditions = [ """>1203</EventID>""", """<TimeCreated SystemTime""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events.Fields} [
    """<Data Name(\\)?=('|")SubjectDomainName('|")>(-|({domain}[^<]+?))<""",
    """Account Domain:\s*(NT AUTHORITY|-|({domain}\S+))\s+Logon ID:""",
    """<Data Name(\\)?=('|")SubjectUserName('|")>(-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))<""",
    """Account Name:\s*(LOCAL SERVICE|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+Account Domain:""",
    """Client IP: ({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """<Computer>({host}[\w\-.]+?)<""",
# audit_type is removed
    """(<|&lt;)AuditResult(&gt;|>)({result}.+?)(&lt;|<)\/AuditResult(&gt;|>)""",
    """(<|&lt;)IpAddress(&gt;|>)({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """(<|&lt;)AuthProtocol(&gt;|>)(N\/A|({protocol}.+?))(&lt;|<)\/AuthProtocol(&gt;|>)""",
# proxy_server is removed
    """(<|&lt;)UserAgentString(&gt;|>)(N\/A|({user_agent}.+?))(<|&lt;)\/UserAgentString(&gt;|>)""",
    """(<|&lt;)Endpoint(&gt;|>)(N\/A|({endpoint}.+?))(<|&lt;)\/Endpoint(&gt;|>)""",
    """(<|&lt;)UserId(&gt;|>)(N\/A|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\&]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(<|&lt;)\/UserId(&gt;|>)"""
    """(<|&lt;)FailureType(&gt;|>)(None|({failure_reason}.+?))(<|&lt;)\/FailureType(&gt;|>)""",
    """(<|&lt;)ErrorCode(&gt;|>)(N\/A|({error_code}.+?))(<|&lt;)\/ErrorCode(&gt;|>)""",
# relying_party is removed
    """(<|&lt;)Server(&gt;|>)(N\/A|({server}.+?))(<|&lt;)\/Server(&gt;|>)""",
# network_location is removed
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)"""
  ]

s-xml-events = {
  ParserVersion = "v1.0.0"
  Vendor = Microsoft
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
  Fields = [
    """<TimeCreated SystemTime\\*=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d{9}Z)"""
    """>({event_code}\d+)</EventID>""",
    """<Security UserID=('|")({user_sid}[^'"]+)('|")\/>""",
    """<Execution ProcessID=('|")({process_id}\d+)('|") ThreadID=('|")({thread_id}\d+)('|")\/>""",
    """<Level>({run_level}[^<]+)<""",
    """<Provider Name =('|")({provider_name}[^'"]+)('|")""",
    """Guid=('|")\{({process_guid}[^\}'"]+?)\}('|")""",
    """<Task>({task_name}[^<]+)""",
    """<Opcode>(0|({opcode}[^<]+))<""",
    """<Keywords>({result}[^<]+)<\/Keywords>""",
    """<EventRecordID>({event_id}[^<]+)""",
    """<Channel>({channel}[^<]+)<"""
  
}
```