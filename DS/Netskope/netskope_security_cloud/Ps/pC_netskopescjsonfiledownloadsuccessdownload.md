#### Parser Content
```Java
{
Name = netskope-sc-json-file-download-success-download
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"type":"""", """"activity":"Download"""", """"object_type":"File"""", """"act_user":"""", """"src-application-name":"Netskope"""" ]
  Fields = [
    """"time":"({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}Z)"""",
    """"activity":"({operation}Download)"""",
    """"src-ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """"app":"({app}[^"]+)"""",
    """"user":"(({email_address}[^@"\s]+@[^@"\s]+\.[^"\s]+)|(({domain}[^"@\\\/\s]+)[\\\/]+)?({user}[^"@\\\/\s]+))"""",
    """"user_name":"(({full_name}[^\\\s"]+\s[^"\\]+)|(({domain}[^"\s\\]+)\\+)?({user}[^"\s]+))"""",
    """"user-email":"({email_address}[^@"]+@[^"\.]+\.[^"]+)""""
   ]
   DupFields = [ "object->file_name" ]
   ParserVersion = v1.0.0


}
```