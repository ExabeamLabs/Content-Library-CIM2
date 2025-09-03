#### Parser Content
```Java
{
Name = unix-unix-kv-alert-trigger-anomloginfailures
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix
  TimeFormat = ["epoch_sec", "MMM dd HH:mm:ss"]
  Conditions = [ """ANOM_LOGIN_FAILURES""", """ msg=""", """ res=""" , """audit""" ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?""",
    """({alert_name}ANOM_LOGIN_FAILURES)""",
    """msg=audit\(({time}\d{10})\.\d{3}""",
    """\sacct="({account_name}[^"]+)"""",
    """\sses=({session_id}\d+)""",
    """\spid=({process_id}\d+)""",
    """\sexe="({process_dir}[^"]+[\/\\])({process_name}[^"\\\/]+?)"""",
    """\suid=({user_id}[^\s]*)\s""",
    """\sauid=({account_id}[^\s]+)\s"""
    """\shostname=(\?|({src_host}[\w\.-]+))\s+\w+=""", 
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```