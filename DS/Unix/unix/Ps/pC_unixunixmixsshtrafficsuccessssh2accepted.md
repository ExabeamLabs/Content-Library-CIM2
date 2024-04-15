#### Parser Content
```Java
{
Name = "unix-unix-mix-ssh-traffic-success-ssh2accepted"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [
    """ ssh2"""
    """Accepted """
    """ for """
    """ from """
  ]
  Fields = [
    """\w{3}\s\d\d\s\d\d:\d\d:\d\d\s(::ffff:)?(Message|({host}[\w\-.]+))\s""",
    """\"host\":\"(::ffff:)?({dest_host}({host}[^\"]+))\""""
    """\"host\":\{\"name\":\"(::ffff:)?({dest_host}({host}[^\"]+))\""""
    """<({time}\d\d\d\d\s+\w{3}\s+\d\d\s+\d\d:\d\d:\d\d)\s"""
    """\d\d:\d\d:\d\d \d\d\d\d (::ffff:)?({host}({dest_host}[^\s]+))"""
    """\s(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\.-]+)):?\s+sshd\["""
    """\d{2}:\d{2}:\d{2}\s+(::ffff:)?({dest_host}[\w\.-]+)\s+auth\|"""
    """Accepted ({auth}\S+) for (({domain}[^\\:]+)\\+)?({user}[\w.'\-\\$]+)(\s|$)"""
    """Accepted ({auth}\S+) for (({user}[^\s@]+?)@({domain}[^\s]+))"""
    """\s+from\s+(::ffff:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\s+from\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """(::ffff:)?({host}[\w.\-]+) sshd ({login_id}\d+)"""
    """(::ffff:)?({host}[\w\.\-]+):\s+sshd\["""
    """sshd\[({login_id}\d+)"""
    """({event_code}ssh)"""
    """\d\d\d\d\s+\w{3}\s+\d\d\s+\d\d:\d\d:\d\d\s+\w+>\s+<(::ffff:)?({dest_host}[\w\-.]+)"""
    """\"computer_name\":\"(::ffff:)?({host}({dest_host}[\w\-.]+))\""""
  ]
  DupFields = [
    "dest_host->original_dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```