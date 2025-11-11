#### Parser Content
```Java
{
Name = microsoft-evadfs-kv-user-password-modify-fail-1205
ParserVersion = "v1.0.0"
Conditions = [
"""EventCode=1205"""
"""SourceName =AD FS Auditing"""
"""A password change was attempted, but failed"""
]
Fields = ${WindowsParsersTemplates.windows-events-6.Fields}[
  """<ClaimsProvider>(?:N\/A|({domain}[^<]+))</ClaimsProvider>"""
  """User=(NULL|NOT_TRANSLATED|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
  """(<|&lt;)IpAddress(&gt;|>)({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """(<|&lt;)UserId(&gt;|>)(N\/A|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\&]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(<|&lt;)\/UserId(&gt;|>)""",
	"""ComputerName =({host}[\w\-.]+)""",
	"""({event_name}A password change was attempted, but failed)""",
]

windows-events-6 = {
  Vendor = Microsoft
  Product = Event Viewer - ADFS
  TimeFormat = ["MM/dd/yyyy hh:mm:ss a", "dd-MM-yyyy HH:mm:ss"]
  Fields = [
    """({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))""",
	"""\WEventCode=({event_code}\d+)""",
	"""\WSourceName =({service_name}.+?)(\s+\w+=|\s*$)""",
	"""RecordNumber=({event_id}\w+)\s*""",
	"""Message=({additional_info}[^:\.]+?)(:|\.)""",
	"""EventType=(|({event_category}[^\s]+))\s""",
	"""Sid=({user_sid}[^\s]+?)\sSidType"""
	""":({service_name}[^:>]+)</RelyingParty>"""
	"""<PrimaryAuth>(N\/A|[^<]+?\/({auth_method}[^<\/]+))</PrimaryAuth>"""
	"""(<|&lt;)AuditType(&gt;|>)({audit_subcategory}.+?)(&lt;|<)\/AuditType(&gt;|>)""",
	"""(<|&lt;)AuditResult(&gt;|>)({result}.+?)(&lt;|<)\/AuditResult(&gt;|>)""",
	"""(<|&lt;)AuthProtocol(&gt;|>)(N\/A|({app_protocol}.+?))(&lt;|<)\/AuthProtocol(&gt;|>)""",
	"""(<|&lt;)ProxyServer(&gt;|>)(N\/A|({proxy_server}.+?))(&lt;|<)\/ProxyServer(&gt;|>)""",
	"""(<|&lt;)UserAgentString(&gt;|>)(N\/A|({user_agent}.+?))(<|&lt;)\/UserAgentString(&gt;|>)""",
	"""(<|&lt;)Endpoint(&gt;|>)(N\/A|({endpoint}.+?))(<|&lt;)\/Endpoint(&gt;|>)""",
	"""(<|&lt;)FailureType(&gt;|>)(None|({failure_reason}.+?))(<|&lt;)\/FailureType(&gt;|>)""",
	"""(<|&lt;)ErrorCode(&gt;|>)(N\/A|({error_code}.+?))(<|&lt;)\/ErrorCode(&gt;|>)""",
	"""(<|&lt;)RelyingParty(&gt;|>)(N\/A|({relying_party}.+?))(<|&lt;)\/RelyingParty(&gt;|>)""",
	"""(<|&lt;)Server(&gt;|>)(N\/A|({server}.+?))(<|&lt;)\/Server(&gt;|>)""",
	"""(<|&lt;)NetworkLocation(&gt;|>)(N\/A|({location_information}.+?))(<|&lt;)\/NetworkLocation(&gt;|>)"""
  
}
```