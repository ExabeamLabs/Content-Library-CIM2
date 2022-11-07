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
    """\srt=({time}\d+)""",
    """\soutcome=({result}.+?)\s+\w+=""",
    """\sdvc=({host}\S+)""",
    """\sdvchost=({host}\S+)""",
    """\saddr\\=(?:\?|({src_ip}\S+))""",
    """\shostname\\=(?:\?|(src_host)\S+)""",
    """\ssrc=({src_ip}\S+)""",
    """\sshost=({src_host}\S+)""",
    """\sduser=({user}.+?)\s+\w+=""",
    """\sact=({auth}\S.+?)\s+\w+=""",
    """\sdproc=({auth_process}\S.+?)\s+\w+=""",
    """({event_code}ssh)""",
  ]
  DupFields = [ "host->dest_host" ]


}
```