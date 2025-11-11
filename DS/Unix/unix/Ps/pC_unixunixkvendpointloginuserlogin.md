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
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """({host}[\w\-\.]+)\saudispd""",
    """msg=audit\(({time}\d{10})\.\d+:\d+\):""",
    """node=({host}[\w\.-]+)\s""",
    """acct="\(?(unknown|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\)?""",
    """hostname=(\?|({src_host}[\w\.-]+))\s+\w+=""", 
    """addr=(\?|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))(:({src_port}\d+))?\s+\w+=""",
    """terminal=(\?|({login_type_text}[^=]+?))\s+\w+=""",
    """exe="({auth_process}[^"]+)""",
    """type=({event_name}USER_\S+)\s+\w+=""",
    """res=({result}[^']+)""",
    """({event_code}ssh)""",
    """({event_name}USER_LOGIN)"""
    """msg='({additional_info}[^']+)'""",
    """pid=({process_id}\d+)""", 
    """uid=({user_id}\d+)""",
    """ses=({session_id}\d+)""",
    """auid=({account_id}\d+)\s"""
    """type=({login_type_text}[^=]+?)\s+\w+="""
  ]
  DupFields = [ "host->dest_host" ]


}
```