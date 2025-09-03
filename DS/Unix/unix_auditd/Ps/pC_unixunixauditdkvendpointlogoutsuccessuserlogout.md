#### Parser Content
```Java
{
Name = unix-unixauditd-kv-endpoint-logout-success-userlogout
  Conditions = [ """ msg=""", """USER_LOGOUT""", """ res=success""", """audit""" ]
  ParserVersion = v1.0.0

unix-audispd-events = {
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = ["epoch_sec", "MMM dd HH:mm:ss"]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """({host}[\w\-\.]+)\saudispd""",
    """\smsg=audit\(({time}\d{10})\.\d+:\d+\):""",
    """\snode=({host}[\w\.-]+)\s""",
    """\shostname=(?:\?|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\.-]+))\s"""
    """\saddr=(\?|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\w+=""",
    """\sres=({result}[^\(\)']+?)('\s*$|'?\s+\w+=)""",
    """\smsg='({additional_info}[^']+)'""",
    """\stype=({event_name}[^=]+?)\s\w+=""",
    """\spid=({process_id}\d+)""", 
    """\suid=({user_id}\d+)""",
    """\sses=({session_id}\d+)""",
    """\sauid=({account_id}\d+)\s""",
    """\sexe="({process_path}({process_dir}[^"]+?)([\/\\]+)({process_name}[^"\/]+))"""",
  ]
  DupFields = [ "host->dest_host" 
}
```