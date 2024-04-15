#### Parser Content
```Java
{
Name = "dropbox-d-json-app-login-success-devices"
Vendor = "Dropbox"
Product = "Dropbox"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
""""event_category": "devices""""
""""info_dict":"""
""""event_type_description":"""
]
Fields = [
""""name":\s*"(?:N\/A|({full_name}[^"@,]+))""""
""""name":\s*"(?:N\/A|(({domain}[^"@\\\s]+)\\+)?({user}[^"@\\\s]+))""""
""""email":\s*"(?:N\/A|({email_address}[^@"\s]+@({email_domain}[^@"\s]+)))"""
""""time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\d:+-]+)""""
""""event_type":\s*"({operation}[^"]+)""""
""""event_type_description":\s*"({additional_info}[^"]+)""""
""""ip_address":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""display_name":\s*"({src_host}[\w\-.]+)\s*""""
""""info_dict":\s*\{[^\}]*?"name":\s*"({app}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```