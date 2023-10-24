#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-forward
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"Operation":""", """"UpdateInboxRules"""", """"ActionType":"Forward"""", """"Workload":""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"(\[)?({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})(\])?(:({src_port}\d+))?""",
    """UserId":"({email_address}[^"\\]+@({email_domain}[^"]+))""",
    """"ActionType":"({operation}[^"]+)"""",
    """destinationServiceName =({app}[^=]+?)\s+\w+=""",
    """\ssourceServiceName =(Core Directory|Account Provisioning|({app}[^=]+?))\s*(\w+=|$)""",
    """"SubjectOrBodyContainsWords":"({filter_key_words}[^"]+)""",
    """flexString1=({event_name}[^=]+?)\s+\w+=""",
    """Forward.+?Recipients\\?":\[?\\?"({dest_email_address}[^\@"]+@({dest_email_domain}[^",;\\]+))"""
    """"ClientInfoString":"({user_agent}[^"]+)""""
  ]


}
```