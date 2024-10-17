#### Parser Content
```Java
{
Name = "unix-unix-kv-ssh-traffic-sshuserauth"
  Vendor = "Unix"
  Product = "Unix Auditd"
  TimeFormat = ["epoch_sec","MM/dd/yyyy HH:mm:ss"]
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
    """acct=\\?"*(\?|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\\?\s*(\w+=|")"""
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
    """\stype=({audispd_type}USER_\S+)\s+\w+="""
    """\sterminal=(\?|({login_type_text}[^=]+?))\s+\w+="""
    """\sexe="({auth_process}[^"]+?)"\s+\w+="""
  ]
  DupFields = [
    "audispd_type->event_name"
  ]
  ParserVersion = "v1.0.0"


}
```