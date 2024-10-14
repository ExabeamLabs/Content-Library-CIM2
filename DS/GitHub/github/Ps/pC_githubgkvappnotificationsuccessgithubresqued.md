#### Parser Content
```Java
{
Name = github-g-kv-app-notification-success-githubresqued
  ParserVersion = v1.0.0
  Vendor = GitHub
  Product = GitHub
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [ """service.name="github-resqued"""", """gh.notification""" ]
  Fields = [
    """\sTimestamp="({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d\d\d\d\d\dZ)""",
    """({host}\S+)\s+github-resqued""",
    """\sgh.notifications.recipient="(?:nil|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
    """\sservice.name="({service_name}[^"]+)"""
    """\sgh.notifications.delivery.comment.type="({additional_info}[^"]+)"""
    """\sBody="({operation}[^"]+)""",
    """({app}github)"""
  ]


}
```