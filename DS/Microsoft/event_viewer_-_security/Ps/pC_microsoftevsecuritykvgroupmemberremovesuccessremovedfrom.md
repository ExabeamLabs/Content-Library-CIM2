#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-remove-success-removedfrom"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch_sec"
  Conditions = [
    """ADAuditPlus"""
    """EVENT_NUMBER = """
    """ was removed from """ 
  ]
  Fields = [
    """TIME_GENERATED\s*=\s*({time}\d{10})"""
    """({host}[\w\-.]+) ADAuditPlus"""
    """CALLER_USER_NAME\s*=\s*({user}[^\s\]]+)"""
    """CALLER_USER_DOMAIN\s*=\s*({domain}[^\s\]]+)"""
    """SOURCE\s*=\s*({src_host}[\w\-.]+)"""
    """EVENT_NUMBER\s*=\s*({event_code}\d+)"""
    """CALLER_LOGON_ID\s*=\s*({login_id}[^\s]+)"""
    """ACCOUNT_SID\s*=\s*\%\{({account_id}[^\s\}]+)"""
    """GROUP_TYPE\s*=\s*({group_type}[^\]]+?)\s*\]"""
    """was removed from .+? Group '({group_name}[^']+)"""
    """MEMBER_NAME\s*=\s*(?:-|({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+)))"""
  ]
  DupFields = [
    "host->dest_host" 
  ]
  ParserVersion = "v1.0.0"


}
```