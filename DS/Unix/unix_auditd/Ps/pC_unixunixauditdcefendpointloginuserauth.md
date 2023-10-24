#### Parser Content
```Java
{
Name = "unix-unixauditd-cef-endpoint-login-userauth"
Conditions = [
"""CEF"""
"""Unix|auditd"""
"""USER_AUTH"""
]
ParserVersion = "v1.0.0"

cef-unix-template-1.Fields}[
    """CEF:([^\|]*\|){4}({event_name}[^|]+)\\""",
    """Arguments:\s*({process_command_line}.*?)\s*cs1Label="""
  ]
  ParserVersion = "v1.0.0"
},

${UnixParsersTemplates.cef-unix-template-1}{
  Name = unix-unixauditd-cef-process-create-success-syscall
  Conditions = [ """CEF""", """Unix|auditd""", """SYSCALL""" ]
  Fields = ${UnixParsersTemplates.cef-unix-template-1.Fields}[
    """CEF:([^\|]*\|){5}({event_name}[^\\\|]+)\|({result}[^\|]+)"""
  ]
  ParserVersion = "v1.0.0"
},

${UnixParsersTemplates.cef-unix-template-1}{
  Name = unix-unixauditd-cef-process-create-success-usercmd
  Conditions = [ """CEF""", """Unix|auditd""", """USER_CMD""" ]
  Fields = ${UnixParsersTemplates.cef-unix-template-1.Fields}[
    """cmd\\=({command}[^\s]+)""",
    """CEF:([^\|]*\|){4}({event_name}[^|]+)\\"""
  ]
  ParserVersion = "v1.0.0"
},
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
    """\sduser=({user}[\w\.\-]{1,40}\$?)\s+\w+=""",
    """\sact=({auth}\S.+?)\s+\w+=""",
    """\sdproc=({auth_process}\S.+?)\s+\w+=""",
    """({event_code}ssh)""",
  ]
  DupFields = [ "host->dest_host" 
}
```