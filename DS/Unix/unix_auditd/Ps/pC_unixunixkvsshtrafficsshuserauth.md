#### Parser Content
```Java
{
Name = "unix-unix-kv-ssh-traffic-sshuserauth"
  Vendor = "Unix"
  Product = "Unix Auditd"
  TimeFormat = "epoch_sec"
  Conditions = [
    """type=USER_AUTH"""
    """PAM:authentication"""
    """terminal=ssh"""
  ]
  Fields = [
    """({time}\d{2}\/\d{2}\/\d{4}\s+\d{2}:\d{2}:\d{2})"""
    """msg=audit\(({time}\d{10})"""
    """\saddr=(?:\?|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[^\s]+))\s"""
    """\d\d:\d\d:\d\d(\.\S+)?\s(::ffff:)?({host}(({dest_ip}(\d{1,3}\.){3}\d{1,3})|({dest_host}[\w\-.]+)))\s"""
    """acct=\\?"*(\?|({user}[^"=]+?))\\?\s*(\w+=|")"""
    """\sres=({result}[^']+)\'"""
    """\sses=\sses=({session_id}\S+?)\s*(\w+=|")"""
    """({event_code}ssh)"""
    """\spid=({process_id}\d+)"""
    """\suid=({user_id}\S+?)\s*(\w+=|")"""
    """auid=({account_id}\S+?)\s*(\w+=|")"""
    """exe=\\?"*({process_dir}[^"=]+?)\\?\s*(\w+=|")"""
    """op=({auth}[^\s=]+)\s"""
    """\sses=({session_id}[^\s=]+?)\s*(\w+=|")"""
    """hostname="*(\?|(({src_ip}(\d{1,3}\.){3}\d{1,3})|({src_host}[^\s]+?)))\s*(\w+=|")"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```