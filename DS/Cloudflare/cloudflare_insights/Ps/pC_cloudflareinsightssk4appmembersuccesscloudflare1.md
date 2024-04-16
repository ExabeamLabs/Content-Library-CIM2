#### Parser Content
```Java
{
Name = cloudflare-insights-sk4-app-member-success-cloudflare-1
  Vendor = Cloudflare
  Product = Cloudflare Insights
  ParserVersion = "v1.0.0"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Conditions = [ """CEF:""", """destinationServiceName =Cloudflare""", """"when":"""" ]
  Fields = [
    """"when":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\.\d{1,7})?Z)"""",
    """destinationServiceName =({app}[^\s]+)""",
    """"ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"actor":\{"email":"({email_address}[^@"]+@[^\."]+\.[^"]+)"""",
    """"account_name":"({account_name}[^"]+)"""",
    """"user_email":"({account}[^"]+)"""",
    """"resource":[^\$]+?"type":"({object_type}[^,"]+)"""",
    """"resource":[^\$]+?"id":"({object_id}[^,"]+)"""",
    """"action":[^\$]+?"result":({result}[^,"]+)""",
    """"action":[^\$]+?"type":"({operation}[^",]+)""""
  ]


}
```