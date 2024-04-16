#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-sshdauthfailed"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """sshd["""
    """[ID """
    """ auth."""
    """] Failed """
  ]
  Fields = [
    """\d\d:\d\d:\d\d (::ffff:)?({host}({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s"""
    """(Failed (none|publickey|keyboard-interactive|password) for (<invalid username>|({user}[\w\.\-]{1,40}\$?)) from ({src_ip}[a-fA-F:\.\d]+)\sport ({src_port}\d+) ssh2)"""
    """Failed (none|publickey|keyboard-interactive) for <({failure_reason}[^>]+)>"""
    """({event_code}ssh)"""
    """({protocol}ssh(d)?)"""
  ]
  ParserVersion = "v1.0.0"


}
```