#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-dlp
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =Netskope""","""alert_type""","""DLP"""]
  Fields =[
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z),""",
      """"dstip"+:"+({dest_ip}[^"]+)"""",
      """"file_type"+:"+({file_type}[^"]+)"""",
      """"app"+:"+({app}[^"]+)"""",
      """"device"+:"+({device_type}[^"]+)"""",
      """"alert_type"+:"+({alert_type}[^"]+)"""",
      """"hostname"+:"+({host}[^"]+)"""",
      """"policy"+:"+({alert_name}[^"]+)"""",
      """"action"+:"+({action}[^"]+)"""",
      """"referer"+:"+({referrer}[^"]+)"""",
      """"user"+:"+({user}[^"]+)"""",
      """"srcip"+:"+({src_ip}[^"]+)"""",
      """"category"+:"+({category}[^"]+)""""
      """"+activity"+:"+({operation}[^"]+)"+""",
      """"object"+:"+({file_name}[^"]+)"""",
      """"+ccl"+:"+({alert_severity}[^"]+)"+""",
      """"+md5"+:"+({hash_md5}[^"]+)"+""",
      """"+request_id"+:({alert_id}[^,]+)""",
      """proto=({protocol}[^"]+)\srequestClientApplication""",
      """outcome=({action}[^ ]+)""",
      """"url":"({url}[^"]+)"""",
      """"from_user"+:"+({from_user_at}[^"]+)"""",
      """"shared_with"+:"+({shared_with_at}[^"]+)"""",
      """"sha256"+:"+({hash_sha256_at}[^"]+)"""",
      """"site"+:"+({site_at}[^"]+)""""
    ]


}
```