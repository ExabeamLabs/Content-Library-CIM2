#### Parser Content
```Java
{
Name = "dropbox-d-json-app-activity-success-shared"
Vendor = "Dropbox"
Product = "Dropbox"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
  """".tag": "shared_"""
  """"event_category":"""
  """"event_type":"""
]
Fields = [
  """"timestamp":\s*"({time}[^"]+)"""
  """"actor":[^\}]*?"display_name":\s*"(?:N\/A|({full_name}[^"@]+))""""
  """"actor":[^\}]*?"email":\s*"(?:N\/A|({email_address}[^@"\s]+@[^@"\s]+))""""
  """"event_type":\s*\{[^\\]*?"\.tag":\s"({operation}[^"]+)""""
  """"description":\s*"({additional_info}[^"]+)""""
  """"ip_address":\s*"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"assets":\s*\[[^\]]*?"display_name":\s*"({object}[^",]+)""""
]
ParserVersion = "v1.0.0"


}
```