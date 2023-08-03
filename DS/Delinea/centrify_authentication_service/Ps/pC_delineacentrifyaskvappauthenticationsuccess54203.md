#### Parser Content
```Java
{
Name = delinea-centrifyas-kv-app-authentication-success-54203
  Vendor = Delinea
  Product = Centrify Authentication Service
  ParserVersion = v1.0.0
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Conditions = [ """SourceName =Centrify AuditTrail""", """AUDIT_TRAIL|Centrify Suite|MFA|""" , """|MFA is skipped|""", """EventCode=54203""" ]
  Fields = [
    """:\d\d\s\w+\s({time}\d\d\/\d\d\/\d\d\d\d\s\d\d:\d\d:\d\d\s(?i)(AM|PM))""",
    """ComputerName =({dest_host}[^\.]+)\.({domain}[^\s]+)""",
    """User=(NOT_TRANSLATED|({user}[\w\.\-]{1,40}\$?))""",
    """Sid=({user_sid}[^\s]+?)\sSidType""",
    """EventCode=({event_code}54203)""",
    """AUDIT_TRAIL\|Centrify Suite\|MFA\|[^=]+({event_name}MFA is skipped)""",
    """reason=({failure_reason}[^=]+)\.?""",
    """Message:\s*({additional_info}[^:]+)\.\s+""",
  ]


}
```