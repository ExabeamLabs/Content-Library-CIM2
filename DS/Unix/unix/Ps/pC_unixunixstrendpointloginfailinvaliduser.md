#### Parser Content
```Java
{
Name = "unix-unix-str-endpoint-login-fail-invaliduser"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ","MMM dd HH:mm:ss"]
  Conditions = [
    """ sshd["""
    """nvalid user """
  ]
  Fields = [
    """({time}\w+\s\d+\s\d+:\d+:\d+)(\s*({host}[\w\-.]+)(\s\w+)?\ssshd\[)?""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[-+]\d+:\d+)?\s*({host}[\w\-.]+)\s*sshd\[""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """\d\d.*?\s({host}[\w\-\.]+)(:|\s|\s\w+)\s*sshd\[\d+\]""",
    """\s({failure_reason}(i|I)nvalid user) ((({domain}[^"\s]+?)\\+)?(?:({email_address}[^"@\s]+@[^"\.\s]+\.[^"\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))?(@({=domain}[^"\s]+))?\s(({src_ip}(\d{1,3}\.){3}\d{1,3})\sport\s({src_port}\d+)\s)?(from |\[preauth\]))?"""
    """\sfrom\s+(::[\w]+:)?({src_ip}(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|::1))(\s+port\s+({src_port}\d+))?\s*"""
    """sshd\[({login_id}\d+)"""
    """({event_code}ssh)"""
    """\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```