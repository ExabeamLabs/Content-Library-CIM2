#### Parser Content
```Java
{
Name = netskope-sc-sk4-alert-trigger-success-dlp
  Vendor = Netskope
  Product = Netskope Security Cloud
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """destinationServiceName =Netskope""",""""alert_type":""",""""DLP"""", """"alert":""", """"yes"""" ]
  Fields =[
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z),""",
      """"dstip"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
      """"file_type"+:"+({file_type}[^"]+)"""",
      """"app"+:"+({app}[^"]+)"""",
      """"device"+:"+({device_type}[^"]+)"""",
      """"alert_type"+:"+({alert_type}[^"]+)"""",
      """"hostname"+:"+({host}[^"]+)"""",
      """"policy"+:"+({alert_name}[^"]+)"""",
      """"action"+:"+({action}[^"]+)"""",
      """"referer"+:"+({referrer}[^"]+)"""",
      """"user"+:"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""",
      """"srcip"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"category"+:"+({category}[^"]+)""""
      """"+activity"+:"+({operation}[^"]+)"+""",
      """"object"+:"+({file_name}[^"]+?(\.({file_ext}\w+))?)"""",
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
      """"dlp_rule_severity":"({alert_severity}[^"]+)""""
      """"dlp_rule_count":({rule_count}\d+)"""
      """"dlp_rule":"({rule}[^"]+)"""
      """"shared_domains":\s*"[\[\<\s]?({domain}[^"\s,\\\]\>]+)"""
    ]


}
```