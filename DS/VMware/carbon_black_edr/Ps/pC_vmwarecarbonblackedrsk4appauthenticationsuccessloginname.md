#### Parser Content
```Java
{
Name = vmware-carbonblackedr-sk4-app-authentication-success-loginname
  Vendor = VMware
  Product = Carbon Black EDR
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"Login in successfully through SAML 2.0"""", """destinationServiceName =Carbon Black Cloud""", """"description":"""", """"loginName":"""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,3}Z)""",
    """"description":"({event_name}[^"]+)"""",
    """"loginName":"({email_address}[^@"]+@[^"\.]+\.[^"]+)"""",
    """"orgName":"({domain}[^"]+)"""",
    """"clientIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  ]


}
```