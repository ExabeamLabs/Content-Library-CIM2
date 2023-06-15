#### Parser Content
```Java
{
Name = unix-ad-cef-endpoint-login-success-userauth
  ParserVersion = v1.0.0
  Vendor = Unix
  Product = Unix Auditd
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Unix|auditd|""", """|USER_AUTH\|success|""", """sshd"""]
  Fields = [
    """\srt=({time}\d{13})""",
    """\soutcome=({result}.+?)\s+\w+=""",
    """\sdvc=({host}\S+)""",
    """\sdvchost=({host}\S+)""",
    """\saddr\\=(?:\?|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\shostname\\=(?:\?|(src_host)\S+)""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sshost=({src_host}\S+)""",
    """\sduser=({user}.+?)\s+\w+=""",
    """\sact=({auth}\S.+?)\s+\w+=""",
    """\sdproc=({auth_process}\S.+?)\s+\w+=""",
    """({event_code}ssh)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```