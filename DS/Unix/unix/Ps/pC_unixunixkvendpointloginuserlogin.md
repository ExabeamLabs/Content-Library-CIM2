#### Parser Content
```Java
{
Name = unix-unix-kv-endpoint-login-userlogin
  Vendor = Unix
  Product = Unix
  ParserVersion = "v1.0.0"
  TimeFormat = ["epoch_sec", "MMM dd HH:mm:ss"]
  Conditions = [ """audit(""", """ type=USER_LOGIN""", """ res=""", """ msg=""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """({host}[\w\-\.]+)\saudispd""",
    """\smsg=audit\(({time}\d{10})\.\d+:\d+\):""",
    """\snode=({host}[\w\.-]+)\s""",
    """\sacct="\(?(unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)?""",
    """\shostname=(\?|({src_host}[\w\.-]+))\s+\w+=""", 
    """\saddr=(\?|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?\s+\w+=""",
    """\sterminal=(\?|({login_type_text}[^=]+?))\s+\w+=""",
    """\sexe="({auth_process}[^"]+)""",
    """\stype=({audispd_type}USER_\S+)\s+\w+=""",
    """\sres=({result}[^\(\)]+?)('\s*$|'?\s+\w+=)""",
    """({event_code}ssh)""",
    """({event_name}USER_LOGIN)"""
    """\smsg='({additional_info}[^']+)'""",
    """\spid=({process_id}\d+)""", 
    """\suid=({user_id}\d+)""",
    """\sses=({session_id}\d+)""",
    """\sauid=({account_id}\d+)\s"""
  ]
  DupFields = [ "host->dest_host" ]


}
```