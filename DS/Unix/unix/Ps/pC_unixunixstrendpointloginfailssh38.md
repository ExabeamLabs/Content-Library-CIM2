#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-ssh38"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """ssh"""
    """<38>"""
    """ Message forwarded from """
  ]
  Fields = [
    """Message forwarded from (::ffff:)?({host}[^\s:]+)"""
    """\ssshd\[[^:]+:\s+({failure_reason}[^=]+?)\s+from(\s+user\s+({user}[\w\.\-]{1,40}\$?))?\s+({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s+port\s+({src_port}\d+)"""
    """({failure_reason}Invalid user) ({user}[\w\.\-]{1,40}\$?) from (::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """input_userauth_request: ({failure_reason}invalid user) ({user}[\w\.\-]{1,40}\$?)"""
    """({protocol}ssh(d)?)"""
    """failed login attempt for ({user}[\w\.\-]{1,40}\$?) from (::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """Login restricted for ({user}[\w\.\-]{1,40}\$?)"""
    """({failure_reason}There have been too many unsuccessful login attempts)"""
  ]
  ParserVersion = "v1.0.0"


}
```