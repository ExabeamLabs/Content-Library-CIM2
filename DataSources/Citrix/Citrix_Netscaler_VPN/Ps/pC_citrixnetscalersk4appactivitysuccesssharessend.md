#### Parser Content
```Java
{
Name = citrix-netscaler-sk4-app-activity-success-sharessend
Vendor = "Citrix"
Product = "Citrix Netscaler VPN"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
  """destinationServiceName =Citrix ShareFile"""
  """dproc=SharesSend"""
  """"CreatorEmail":"""
]
Fields = [
  """"CreationDate":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  """"Name":"({file_path}({file_dir}[^"]*?[\/]+)?({file_name}[^\/"]+?(\.({file_ext}[^\/"]+))?))""""
  """destinationServiceName =({app}[^=]+?)\s+\w+="""
  """dproc=({operation}[^\s]+)"""
  """"RecipientEmail":"({target}[^"]+)""""
  """"CreatorEmail":"({email_address}[^@"]+@({email_domain}[^@"]+))""""
]
ParserVersion = "v1.0.0"


}
```