#### Parser Content
```Java
{
Name = amazon-awscloudtrail-sk4-app-authentication-success-cloudtrail
  Vendor = Amazon
  Product = AWS CloudTrail
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """destinationServiceName =AWS""", """dproc=cloud-trail""" ]
  Fields = [
    """"eventTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"eventType":"({operation}[^"]+)""",
    """eventName":"({event_name}[^"]+)""",
    """dproc=({app}[^=]+?)\s+(\w+=|$)""",
    """destinationServiceName =({service_name}[^=]+?)\s+(\w+=|$)""",
    """"+userIdentity.+?AssumedRole.+?principalId\\?"+\s*:\s*\\?"+?[A-Z\d]{1,50}:(({email_address}[^@"]+@[^@"]+)|({user}[\w\.\-]{1,40}\$?))\\?"+\s*[,\]\}]""",
    """"userName"+\s*:\s*"+?(|({email_address}[^@"]+@[^@".]+\.[^@"]+)|({user}[\w\.\-]{1,40}\$?))"+\s*[,\]\}]""",
    """"sourceIPAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"userAgent":"({user_agent}[^"]+)""",
    """"awsRegion":"({region}[^"]+)"""",
  ]
  ParserVersion = v1.0.0


}
```