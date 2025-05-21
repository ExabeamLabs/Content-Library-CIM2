#### Parser Content
```Java
{
Name = vmware-carbonblackedr-sk4-app-notification-success-carbonblackcloud
  Vendor = VMware
  Product = Carbon Black EDR
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =Carbon Black Cloud""", """"description":"""", """"loginName":""", """"orgName":"""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
    """"description":"({additional_info}[^"]+)"""",
    """"loginName":"({email_address}[^@"]+@[^"\.]+\.[^"]+)"""",
    """"orgName":"({domain}[^"]+)"""",
    """"ClientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  ]


}
```