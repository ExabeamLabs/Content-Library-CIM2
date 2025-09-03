#### Parser Content
```Java
{
Name = juniper-jn-kv-app-login-fail-sshdloginfailed
  Vendor = Juniper Networks
  Product = Junos OS
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ sshd - SSHD_LOGIN_FAILED""", """ Login failed""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\-|\+)\d\d:\d\d) ({host}[\w\-.]+) sshd - SSHD_LOGIN_FAILED""",
    """username="({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """source-address="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```