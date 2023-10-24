#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-invaliduser"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """ sshd["""
    """nvalid user """
  ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\s({host}[\w\.-]+):?\s+sshd\["""
    """({failure_reason}(i|I)nvalid user)\s+(({domain}[^"\s]+?)\\+)?(?:({email_address}[^"@\s]+@[^"\.\s]+\.[^"\s]+)|({user}[\w\.\-]{1,40}\$?))(@({=domain}[^"\s]+))?"""
    """\sfrom\s+(::[\w]+:)?(({src_ip}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|::1))|({src_host}[\w\.\-]+))\s*"""
    """sshd\[({login_id}\d+)"""
    """({event_code}ssh)"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```