#### Parser Content
```Java
{
Name = unix-unixauditd-kv-endpoint-logout-success-userlogout
  Conditions = [ """ audispd""", """type=USER_LOGOUT""", """ res=""", """ msg=""" ]
  ParserVersion = v1.0.0

unix-audispd-events = {
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "epoch_sec"
  Fields = [
    """({host}[\w\-\.]+)\saudispd""",
    """\smsg=audit\(({time}\d{10})\.\d+:\d+\):""",
    """\snode=({host}[\w\.-]+)\s""",
    """\shostname=(\?|({src_host}[\w\.-]+))\s+\w+=""",
    """\saddr=(\?|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\w+=""",
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