#### Parser Content
```Java
{
Name = microsoft-evsecurity-xml-app-authentication-fail-1203-1
  ParserVersion = "v1.0.0"
  Conditions = [ """(EventID 1203)""", """<NetworkLocation>""", """<AuthProtocol>""" ]
  Fields = ${DLWindowsParsersTemplates.s-xml-events-1.Fields}[
    """({host}[\w.-]+)\sMSWinEventLog\s""",
    """({event_name}The Federation Service failed to validate a new credential)"""
  ]

s-xml-events-1 = {
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Fields = [
    """MSWinEventLog\s.+?\s({time}\w{3}\s\d{2}\s(\d{2}:){2}\d{2}\s\d{4})""",
    """\(EventID\s({event_code}\d+)\)""",
    """(<|&lt;)AuditType(&gt;|>)({audit_subcategory}.+?)(&lt;|<)\/AuditType(&gt;|>)""",
    """(<|&lt;)AuditResult(&gt;|>)({result}.+?)(&lt;|<)\/AuditResult(&gt;|>)""",
    """(<|&lt;)IpAddress(&gt;|>)({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """(<|&lt;)AuthProtocol(&gt;|>)(N\/A|({app_protocol}.+?))(&lt;|<)\/AuthProtocol(&gt;|>)""",
    """(<|&lt;)ProxyServer(&gt;|>)(N\/A|({proxy_server}.+?))(&lt;|<)\/ProxyServer(&gt;|>)""",
    """(<|&lt;)UserAgentString(&gt;|>)(N\/A|({user_agent}.+?))(<|&lt;)\/UserAgentString(&gt;|>)""",
    """(<|&lt;)Endpoint(&gt;|>)(N\/A|({endpoint}.+?))(<|&lt;)\/Endpoint(&gt;|>)""",
    """(<|&lt;)UserId(&gt;|>)(N\/A|({email_address}[^@&]+@[^&]+)|(({domain}[^\\&]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(<|&lt;)\/UserId(&gt;|>)""",
    """(<|&lt;)FailureType(&gt;|>)(None|({failure_reason}.+?))(<|&lt;)\/FailureType(&gt;|>)""",
    """(<|&lt;)ErrorCode(&gt;|>)(N\/A|({error_code}.+?))(<|&lt;)\/ErrorCode(&gt;|>)""",
    """(<|&lt;)RelyingParty(&gt;|>)(N\/A|({relying_party}.+?))(<|&lt;)\/RelyingParty(&gt;|>)""",
    """(<|&lt;)Server(&gt;|>)(N\/A|({server}.+?))(<|&lt;)\/Server(&gt;|>)""",
    """(<|&lt;)NetworkLocation(&gt;|>)(N\/A|({location_information}.+?))(<|&lt;)\/NetworkLocation(&gt;|>)"""
    """<Level>({run_level}[^<]+)<"""
  
}
```