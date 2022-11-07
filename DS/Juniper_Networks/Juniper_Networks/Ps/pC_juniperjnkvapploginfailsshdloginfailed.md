#### Parser Content
```Java
{
Name = juniper-jn-kv-app-login-fail-sshdloginfailed
  Vendor = Juniper Networks
  Product = Juniper Networks
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ sshd - SSHD_LOGIN_FAILED""", """ Login failed""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\-|\+)\d\d:\d\d) ({host}[\w\-.]+) sshd - SSHD_LOGIN_FAILED""",
    """username="({user}[^"\s]+)""",
    """source-address="({src_ip}[A-Fa-f:\d.]+)""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```