#### Parser Content
```Java
{
Name = microsoft-o365-sk4-app-activity-success-forwardto
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""New-InboxRule""" , """ForwardTo""" ]
  Fields = [
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
    """Forward.+?Value":"(smtp:)?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
    """"ResultStatus":"({result}[^"]+)"""",
    """"ClientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({operation}ForwardTo)"""",
    """msg=({additional_info}.+?)\srequest=""",
    """UserId":"({email_address}[^"\\]+@({email_domain}[^"]+))""",
    """destinationServiceName =({app}.+?)\s(device|filePath)""",
    """({app}Office 365)"""
    """\ssourceServiceName =(Core Directory|Account Provisioning|({app}[^=]+?))\s+(\w+=|$)""",
    """"SubjectOrBodyContainsWords":"({filter_key_words}[^"]+)"""
    """"ObjectId":"(Unknown|Not Available|({object}[^"]+?))\s*""""
    """"CorrelationId":\s*"({correlation_id}[^"]+)""""
  ]


}
```