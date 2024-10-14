#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-add-success-adauditplus"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """ADAuditPlus"""
    """EVENT_NUMBER = """
    """REMARKS = A member was added to """
  ]
  Fields = [

    """({host}[\w\-.]+) ADAuditPlus"""
    """CALLER_USER_NAME\s*=\s*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """CALLER_USER_DOMAIN\s*=\s*({domain}[^\s\]]+)"""
    """SOURCE\s*=\s*({src_host}[\w\-.]+)"""
    """EVENT_NUMBER\s*=\s*({event_code}\d+)"""
    """CALLER_LOGON_ID\s*=\s*({login_id}[^\s]+)"""
    """ACCOUNT_SID\s*=\s*\%\{(({user_sid}S-\d+-[^\s\}]+)|({account_id}[^\s\}]+))"""
    """GROUP_TYPE\s*=\s*({group_type}[^\]]+?)\s*\]"""
    """was added to .+? Group '({group_name}[^']+)"""
    """MEMBER_NAME\s*=\s*(?:-|({user_dn}CN=.+?,({user_ou}OU.+?DC=[\w-]+)))"""
    """MEMBER_SID\s*=\s*({dest_user_sid}S-\d+-[^\s\]]+)"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```