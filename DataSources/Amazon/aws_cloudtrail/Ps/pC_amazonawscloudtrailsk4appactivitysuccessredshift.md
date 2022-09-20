#### Parser Content
```Java
{
Name = amazon-awscloudtrail-sk4-app-activity-success-redshift
  Vendor = Amazon
  Product = aws cloudtrail
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """destinationServiceName =AWS""", """dproc=Redshift""" ]
  Fields = [
    """"date":"*({time}\d+)"?""",
    """suser=({user}\S+)""",
    """suid=({user_id}\S+)""",
    """"message":"({additional_info}[^"]+?)"""",
    """"severity":"({severity}[^"]+?)"""",
    """"eventId":"({event_name}[^"]+?)"""",
    """"eventCategories":\[?({categories}[^\]]+)\]?""",
    """dproc=({app}Redshift)""",
    """"sourceType":"({source_type}[^"]+?)"""",
    """"sourceIdentifier":"({src_host}[^"]+?)""""
  ]
  ParserVersion = "v1.0.0"


}
```