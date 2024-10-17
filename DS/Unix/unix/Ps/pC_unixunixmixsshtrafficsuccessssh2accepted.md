#### Parser Content
```Java
{
Name = "unix-unix-mix-ssh-traffic-success-ssh2accepted"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy/MM/dd HH:mm:ss","yyyy MMM dd HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ","MMM dd HH:mm:ss"]
  Conditions = [
    """ ssh2"""
    """Accepted """
    """ for """
    """ from """
  ]
  Fields = [
    """\d\d:\d\d:\d\d\s+(::ffff:)?(({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|(\d\S+|tag_audit_log|({host}[\w.\-]+)))\s+(\d\S+|tag_audit_log|({=host}[\w.\-]+)\s)?"""
    """\s({host}({dest_host}[\w\-\.]+))\s({additional_info}Accepted[^:]+?\d{1,5})(\s\w+)?\s*ssh2""",
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s(::ffff:)?(Message|({host}[\w\-.]+))\s""",
    """\"host\":\"(::ffff:)?({dest_host}({host}[^\"]+))\""""
    """\"host\":\{\"name\":\"(::ffff:)?({dest_host}({host}[^\"]+))\""""
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(.\d\d\d)?[\+\-][^\s]+)""",
    """<({time}\d\d\d\d\s+\w{3}\s+\d\d\s+\d\d:\d\d:\d\d)\s"""
    """({time}\d\d\d\d\/\d\d\/\d\d\s\d\d:\d\d:\d\d),"""
    """\d\d:\d\d:\d\d \d\d\d\d (::ffff:)?({host}({dest_host}[^\s]+))"""
    """\s(::ffff:)?({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w\.-]+)):?\s+sshd\["""
    """\d{2}:\d{2}:\d{2}\s+(::ffff:)?({dest_host}[\w\.-]+)\s+auth\|"""
    """Accepted ({auth}\S+) for (({domain}[^\\:]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s|$)"""
    """Accepted ({auth}\S+) for (({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s]+))"""
    """\s+from\s+(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\s+from\s+(::[\w]+:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\d\d\s(::ffff:)?({host}[\w.\-]+) sshd ({login_id}\d+)"""
    """\d\d\s(::ffff:)?({host}[\w\.\-]+)(:|\s|\s\w+)\s*sshd\["""
    """sshd\[({login_id}\d+)"""
    """({event_code}ssh)"""
    """\d\d\d\d\s+\w{3}\s+\d\d\s+\d\d:\d\d:\d\d\s+\w+>\s+<(::ffff:)?({dest_host}[\w\-.]+)"""
    """\"computer_name\":\"(::ffff:)?({host}({dest_host}[\w\-.]+))\"""",
    """\sfrom[^:]+?\sport\s({src_port}\d+)"""
    """@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""""
  ]
  DupFields = [
    "dest_host->original_dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```