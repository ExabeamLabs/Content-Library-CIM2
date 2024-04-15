#### Parser Content
```Java
{
Name = "unix-unix-kv-endpoint-login-sshdauth"
  Vendor = "Unix"
  Product = "Unix"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [
    """pam_"""
    """(sshd:auth):"""
    """authentication"""
    """tty=ssh"""
  ]
  Fields = [
    """\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d\s+({host}[\w\.-]+)\s+[^=]+?pam_(sss|unix)\(sshd:auth\):"""
    """timestamp\":\"({time}\d{4}-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3})"""
    """pam_(sss|unix)\(sshd:auth\):\s+authentication\s+({result}success|failure);"""
    """({event_code}ssh)"""
    """\srhost=(?:({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-.]+))\s"""
    """\suser=(({domain}[^\\=\s\"]+?)\\+)?({user}[^\s>=\"]+)"""
    """sshd\[({login_id}\d+)"""
    """\d{4}\s+\w{3}\s+\d{1,2}\s+\d\d:\d\d:\d\d\s+\w+>\s+<({dest_host}[\w\-.]+)"""
    """\"+_time\"+:\"+({time}[^\"]+)\"+"""
    """\suid=({user_id}[^\s]+)\s"""
  ]
  ParserVersion = "v1.0.0"


}
```