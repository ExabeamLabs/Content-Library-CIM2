#### Parser Content
```Java
{
Name = dropbox-d-json-app-activity-success-apps
    Vendor = Dropbox
    Product = Dropbox
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = [ """"event_category": "apps"""", """"info_dict":""", """"event_type_description":""" ]
    Fields = [
      """"name":\s*"(?:N\/A|({full_name}[^"@,]+))"""",
      """"name":\s*"(?:N\/A|(({domain}[^"@\\\s]+)\\+)?({user}[^"@\\\s]+))"""",
      """"email":\s*"(?:N\/A|({email_address}[^@"\s]+@({email_domain}[^@"\s]+)))""",
      """"time":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[\d:+-]+)"""",
      """"event_type":\s*"({operation}[^"]+)"""",
      """"event_type_description":\s*"({additional_info}[^"]+)"""",
      """"ip_address":\s*"({src_ip}[a-fA-F\d.:]+)""",
      """"info_dict":\s*\{[^\}]*?"name":\s*"({app}[^"]+)""""
    ]
	ParserVersion = "v1.0.0"
  

}
```