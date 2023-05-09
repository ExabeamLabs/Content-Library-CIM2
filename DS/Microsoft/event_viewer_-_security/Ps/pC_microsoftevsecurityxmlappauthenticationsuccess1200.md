#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-app-authentication-success-1200
  ParserVersion = "v1.0.0"
  Conditions = [ """(EventID 1200)""", """MSWinEventLog""", """AD FS Auditing""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events-1.Fields}[
    """({event_name}The Federation Service issued a valid token)"""
  ]

s-xml-events-1 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """MSWinEventLog\s.+?\s({time}\w{3}\s\d{2}\s(\d{2}:){2}\d{2}\s\d{4})""",
    """({host}[\w.-]+)\sMSWinEventLog\s""",
    """\(EventID\s({event_code}\d+)\)""",
    """(<|&lt;)AuditType(&gt;|>)({audit_type}.+?)(&lt;|<)\/AuditType(&gt;|>)""",
    """(<|&lt;)AuditResult(&gt;|>)({audit_result}.+?)(&lt;|<)\/AuditResult(&gt;|>)""",
    """(<|&lt;)IpAddress(&gt;|>)({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """(<|&lt;)AuthProtocol(&gt;|>)(N\/A|({auth_protocol}.+?))(&lt;|<)\/AuthProtocol(&gt;|>)""",
    """(<|&lt;)ProxyServer(&gt;|>)(N\/A|({proxy_server}.+?))(&lt;|<)\/ProxyServer(&gt;|>)""",
    """(<|&lt;)UserAgentString(&gt;|>)(N\/A|({user_agent}.+?))(<|&lt;)\/UserAgentString(&gt;|>)""",
    """(<|&lt;)Endpoint(&gt;|>)(N\/A|({endpoint}.+?))(<|&lt;)\/Endpoint(&gt;|>)""",
    """(<|&lt;)UserId(&gt;|>)(N\/A|({email_address}[^@&]+@[^&]+)|(({domain}[^\\&]+)\\+)?({user}[^\\&]+))(<|&lt;)\/UserId(&gt;|>)""",
    """(<|&lt;)FailureType(&gt;|>)(None|({failure_reason}.+?))(<|&lt;)\/FailureType(&gt;|>)""",
    """(<|&lt;)ErrorCode(&gt;|>)(N\/A|({error_code}.+?))(<|&lt;)\/ErrorCode(&gt;|>)""",
    """(<|&lt;)RelyingParty(&gt;|>)(N\/A|({relying_party}.+?))(<|&lt;)\/RelyingParty(&gt;|>)""",
    """(<|&lt;)Server(&gt;|>)(N\/A|({server}.+?))(<|&lt;)\/Server(&gt;|>)""",
    """(<|&lt;)NetworkLocation(&gt;|>)(N\/A|({network_location}.+?))(<|&lt;)\/NetworkLocation(&gt;|>)"""
  
}
```