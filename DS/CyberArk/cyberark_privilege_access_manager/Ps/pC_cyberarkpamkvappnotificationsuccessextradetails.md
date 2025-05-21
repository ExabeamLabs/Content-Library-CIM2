#### Parser Content
```Java
{
Name = cyberark-pam-kv-app-notification-success-extradetails
  Vendor = CyberArk
  Product = "CyberArk Privilege Access Manager"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ExtraDetails=""", """reason=""", """app=""", """CAPolicy=""", """externalId=""" ]
  Fields = [
  """GatewayStation=({gateway_station}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """shost=(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?|({src_host}[\w\-\.]+))"""
  """duser=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """username=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
  """ExtraDetails=({additional_info}[^;\s]+)"""
  ]
  ParserVersion = v1.0.0


}
```