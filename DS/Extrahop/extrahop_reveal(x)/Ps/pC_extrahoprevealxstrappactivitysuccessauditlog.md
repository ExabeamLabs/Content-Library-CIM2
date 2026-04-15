#### Parser Content
```Java
{
Name = "extrahop-revealx-str-app-activity-success-auditlog"
  Vendor = "Extrahop"
  Product = "Extrahop Reveal(x)"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """name="Audit log"""", """facility="""", """operation="""", """details= {""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{3}Z)\s*({host}[\w.-]+)\s"""
    """details=\{.*?"details":\s*"({description}[^"]+)""""
    """user="(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """operation="({operation}({action}[^"]+))""""
    """"priority"=(null|("|)({severity}[^"]+)("|)),"""
    """"src_ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """facility="({category}[^"]+)""""
  ]
  ParserVersion = "v1.0.0"


}
```