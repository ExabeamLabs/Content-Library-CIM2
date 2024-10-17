#### Parser Content
```Java
{
Name = "unix-unix-kv-ssh-traffic-audispd"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["epoch_sec", "MMM dd HH:mm:ss"]
  Conditions = [
    """ msg=audit("""
    """ type=USER_"""
    """ uid="""
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\s({dest_host}[\w\-.]+)\s+audispd:"""
    """\smsg=audit\(({time}\d{10})\.\d+:\d+\):"""
    """\snode=({dest_host}[\w\.-]+)\s"""
    """\sacct="\(?(unknown|(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\)?"\s+\w+="""
    """\shostname=(\?|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\.-]+))\s+\w+="""
    """\saddr=(\?|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\w+="""
    """\sterminal=(\?|({login_type_text}[^=]+?))\s+\w+="""
    """\sexe="({auth_process}[^"]+?)"\s+\w+="""
    """\sgrantors=({auth_process}[^=]+?)\s+\w+="""
    """\stype=({audispd_type}USER_\S+)\s+\w+="""
    """\sres=({result}[^\(\)]+?)('\s*$|'?\s+\w+=)"""
    """({event_code}ssh)"""
    """op=({action}[^\s]+)"""
    """\smsg='({additional_info}[^']+)'""",
  ]
  DupFields = [
    "dest_host->host",
    "audispd_type->event_name"
  ]
  ParserVersion = "v1.0.0"


}
```