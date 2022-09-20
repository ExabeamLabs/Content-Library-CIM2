#### Parser Content
```Java
{
Name = mimecast-es-sk4-app-activity-success-auditevents
  Vendor = Mimecast
  Product = Email Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"auditType":""", """destinationServiceName =Mimecast Email Security""", """dproc=Audit Events""", """"category":""" ]
  Fields = [
    """"eventTime":"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}(\+|-)\d+?)"""",
    """user":"(|({email_address}[^@"]+@({email_domain}[^@"]+))|({user}[^",]+?))"""",
    """"eventInfo":"({additional_info}[^"]*?)("|\s*$)""",
    """Application:\s*({app}[^",=:]+?)("|,|\s\S+=|\s\S+:)""",
    """\sIP:\s*({src_ip}[a-fA-F\d\.:]+?)\s""",
    """"category":"({category}[^",\}]+?)"""",
    """"auditType":"({operation}[^",]+?)""""
  ]
  ParserVersion = "v1.0.0"


}
```