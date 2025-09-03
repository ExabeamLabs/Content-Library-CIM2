#### Parser Content
```Java
{
Name = mimecast-seg-sk4-app-activity-success-auditevents
  Vendor = Mimecast
  Product = Mimecast Secure Email Gateway
  Conditions = [ """"auditType":""", """"eventTime":""", """"eventInfo":""", """"category":""" ]
  Fields = ${mimecast-json-template.mimecast-json-event.Fields}[
    """"eventTime":"({time}\d{4}-\d{2}-\d{2}T(\d{2}:){2}\d{2}(\+|-)\d+?)"""",
    """"user":"(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))(?<!local)(?<!loc)(?<!prd)(?<!localdomain)|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(?:@({domain}[^,"]+)[^"]*)?)"""",
    """"eventInfo":"({additional_info}[^"]*?)("|\s*$)""",
    """Application:\s*({app}[^",=:]+?)("|,|\s\S+=|\s\S+:)""",
    """\sIP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """"category":"({category}[^",\}]+?)"""",
    """"auditType":"({operation}[^",]+?)""""
  ]
  ParserVersion = "v1.0.0"


}
```