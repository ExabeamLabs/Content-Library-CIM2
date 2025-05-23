#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-login-success-userauth"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "MMM dd HH:mm:ss"]
  Conditions = [
    """type=USER_AUTH"""
    """PAM:authentication"""
    """terminal="""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """,({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2})"""
    """\w{3}\s\d{2}\s\d{2}:\d{2}:\d{2}\s({host}[\w.-]+)\stype=USER_AUTH"""
    """({host}[\w\-.]+)\s*tag_audit_log:"""
    """({time}\d{2}\/\d{2}\/\d{4}\s+\d{2}:\d{2}:\d{2})"""
    """msg=audit\(({time}\d{10})"""
    """\spid=({process_id}\d+)"""
    """\suid=({user_id}\S+?)\s*(\w+=|\")"""
    """auid=({account_id}\S+?)\s*(\w+=|\")"""
    """ses=({session_id}\S+?)\s*(\w+=|\")"""
    """acct=\\?"*(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?\s*(\w+=|")"""
    """exe=\\?"*({process_dir}[^"=]+?)\\?\s*(\w+=|")"""
    """res=\\?"*({result}[^'\s]+)"""
    """\s*({host}[\w\-.]+)\s(auditlog|audispd|audisp-syslog)"""
    """hostname="*(\?|({src_ip}(\d{1,3}\.){3}\d{1,3})|({src_host}[^\s]+?))\s*(\w+=|")"""
    """\stype=({audispd_type}USER_\S+)\s+\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```