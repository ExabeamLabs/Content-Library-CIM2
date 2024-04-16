#### Parser Content
```Java
{
Name = pingidentity-pinga-kv-http-session
  Vendor = Ping Identity
  Product = Ping Access
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions= [ """exchangeId="""", """trackingId="""", """roundTripMS="""", """authMech="""", """responseCode="""" ]
  Fields=[
    """({host}\w+)\s({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""",
    """client="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """method="({method}[^"]+)"""",
    """requestUri="({uri_path}[^"]+)"""",
    """responseCode="({http_response_code}\d+)"""",
    """targetHost="(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+)?)|({url}[^"]+))"""", 
    """subject="({user}[^"]+)"""",
    """applicationName ="({app}[^"]+)""""
  ]
  ParserVersion = "v1.0.0" 


}
```