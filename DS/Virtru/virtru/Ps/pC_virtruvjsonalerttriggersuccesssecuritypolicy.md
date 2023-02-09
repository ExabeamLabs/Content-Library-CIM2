#### Parser Content
```Java
{
Name = virtru-v-json-alert-trigger-success-security-policy
  Vendor = Virtru
  Product = Virtru
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [ """"accessedBy":""", """"policyType":""", """"forwardLog":""", """"recipients":""", """"sender":""", """virtru""" ]
  Fields = [
     """"lastModified"+:\s+"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""",
     """"recipients"+:\s+\[([\s\n]*)?"+({recipient}[^"\s,@]+@[^"\s@,]+)""",
     """"sender"+:\s+"+({sender}[^"\s@]+@[^"\s@]+)"""",
     """"requestIp"+:\s"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
     """"policyId"+:\s+"+({alert_id}[^"]+)"""",
     """"policyType"+:\s+"+({alert_name}[^"]+)"""",
     """"userAgent"+:\s+"+({user_agent}[^"]+)"""",
     """"displayName"+:\s+"+\s+({additional_info}[^"]+?)\s+"""",
     """"type"+:\s+"+({alert_type}[^"]+)""""
  ]


}
```