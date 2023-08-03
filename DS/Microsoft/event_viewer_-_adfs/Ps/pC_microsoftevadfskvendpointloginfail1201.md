#### Parser Content
```Java
{
Name = microsoft-evadfs-kv-endpoint-login-fail-1201
ParserVersion = "v1.0.0"
Conditions = [
"""EventCode=1201"""
"""SourceName =AD FS Auditing"""
"""ComputerName ="""
"""Message=The Federation Service failed to issue a valid token"""
]
Fields = ${WindowsParsersTemplates.windows-events-6.Fields}[
	"""({event_name}The Federation Service failed to issue a valid token)""",
]

windows-events-6 = {
  Vendor = Microsoft
  Product = Event Viewer - ADFS
  TimeFormat = "dd-MM-yyyy HH:mm:ss"
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d (AM|PM|am|pm))""",
	"""\WEventCode=({event_code}\d+)""",
	"""ComputerName =({host}[\w\-.]+)""",
	"""\WSourceName =({service_name}.+?)(\s+\w+=|\s*$)""",
	"""RecordNumber=({event_id}\w+)\s*""",
	"""Message=({additional_info}[^:\.]+?)(:|\.)""",
	"""EventType=(|({event_category}[^\s]+))\s""",
	"""User=(NULL|NOT_TRANSLATED|({user}[\w\.\-]{1,40}\$?))""",
	"""Sid=({user_sid}[^\s]+?)\sSidType"""
	"""<ClaimsProvider>(?:N\/A|({domain}[^<]+))</ClaimsProvider>"""
	""":({service_name}[^:>]+)</RelyingParty>"""
	"""<PrimaryAuth>(N\/A|[^<]+?\/({auth_method}[^<\/]+))</PrimaryAuth>"""
	"""(<|&lt;)AuditType(&gt;|>)({audit_type}.+?)(&lt;|<)\/AuditType(&gt;|>)""",
	"""(<|&lt;)AuditResult(&gt;|>)({audit_result}.+?)(&lt;|<)\/AuditResult(&gt;|>)""",
	"""(<|&lt;)IpAddress(&gt;|>)({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
	"""(<|&lt;)AuthProtocol(&gt;|>)(N\/A|({auth_protocol}.+?))(&lt;|<)\/AuthProtocol(&gt;|>)""",
	"""(<|&lt;)ProxyServer(&gt;|>)(N\/A|({proxy_server}.+?))(&lt;|<)\/ProxyServer(&gt;|>)""",
	"""(<|&lt;)UserAgentString(&gt;|>)(N\/A|({user_agent}.+?))(<|&lt;)\/UserAgentString(&gt;|>)""",
	"""(<|&lt;)Endpoint(&gt;|>)(N\/A|({endpoint}.+?))(<|&lt;)\/Endpoint(&gt;|>)""",
	"""(<|&lt;)UserId(&gt;|>)(N\/A|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\&]+)\\+)?({user}[^\\&]+))(<|&lt;)\/UserId(&gt;|>)""",
	"""(<|&lt;)FailureType(&gt;|>)(None|({failure_reason}.+?))(<|&lt;)\/FailureType(&gt;|>)""",
	"""(<|&lt;)ErrorCode(&gt;|>)(N\/A|({error_code}.+?))(<|&lt;)\/ErrorCode(&gt;|>)""",
	"""(<|&lt;)RelyingParty(&gt;|>)(N\/A|({relying_party}.+?))(<|&lt;)\/RelyingParty(&gt;|>)""",
	"""(<|&lt;)Server(&gt;|>)(N\/A|({server}.+?))(<|&lt;)\/Server(&gt;|>)""",
	"""(<|&lt;)NetworkLocation(&gt;|>)(N\/A|({network_location}.+?))(<|&lt;)\/NetworkLocation(&gt;|>)"""
  
}
```