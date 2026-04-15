#### Parser Content
```Java
{
Name = zscaler-pa-str-vpn-login-success-authenticate
  ParserVersion = v1.0.0
  Vendor = Zscaler
  Product = Zscaler Private Access
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""",ZPN_STATUS_AUTHENTICATED,""",""" Status zpa-lss:"""]
  Fields = [
    """([^,]*,){2}((({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?(@({domain}[^,]+))?)),)?([^,]*,){6}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))?,([^,]*,){2}({country_code}\w+),({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ),[^,]*,({bytes_in}\d+),({bytes_out}\d+)"""
    """User Status zpa-lss: ,([^,]*,){2}({session_id}[^,]+),({event_name}[^,]+),([^,]*,){3}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))?,({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))?,"""
    """User Status zpa-lss: ,([^,]*,){16}({auth_method}[^,]+),({host}[^,][\w\.\-]+),({os}[^,]+),({client_type}[^,]+),"""
  ]


}
```