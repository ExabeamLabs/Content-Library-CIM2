#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-login-sshdauth"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","MMM dd HH:mm:ss","MMM d HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [
    """pam_"""
    """(sshd:auth):"""
    """authentication"""
    """tty=ssh"""
  ]
  Fields = [
    """({time}\w+\s+\d+\s+\d+:\d+:\d+)\s+({host}[\w\.-]+)\s+[^=]+?pam_(sss|unix)\(sshd:auth\):"""
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+[-+]\d+:\d+)\s+({host}[\w\.-]+)\s+[^=]+?pam_(sss|unix)\(sshd:auth\):"""
    """>({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
    """timestamp\":\"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""
    """pam_(sss|unix)\(sshd:auth\):\s+({event_name}authentication\s+({result}success|failure));"""
    """({event_code}ssh)"""
    """\srhost=(?:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))\s"""
    """\suser=(({domain}[^\\=\s\"]+?)\\+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """sshd\[({login_id}\d+)"""
    """\d{4}\s+\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d\s+\w+>\s+<({dest_host}[\w\-.]+)"""
    """\w{3}\s*\d+\s\d+:\d+:\d+\s({dest_host}[\w\-.]+)\s"""
    """(\d+[-+]\d+:\d+)\s+({dest_host}[\w\.-]+)\s+"""
    """\"+_time\"+:\"+({time}[^\"]+)\"+"""
    """\suid=({user_id}[^\s]+)\s"""
  ]
  ParserVersion = "v1.0.0"


}
```