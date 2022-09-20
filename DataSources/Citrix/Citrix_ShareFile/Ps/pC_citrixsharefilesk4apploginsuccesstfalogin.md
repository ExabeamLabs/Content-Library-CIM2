#### Parser Content
```Java
{
Name = citrix-sharefile-sk4-app-login-success-tfalogin
  Vendor = Citrix
  Product =  Citrix ShareFile
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""destinationServiceName =Citrix ShareFile""",""""Activity":"TFA_Login"""", """"Email":"""]
  Fields = [
    """"Date"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"Email":"({email_address}[^@"]+@({email_domain}[^@"]+))"""",
    """"IPAddress"+:"+({src_ip}[A-Fa-f\d:.]+)"""",
    """"+EventID"+:"+({event_code}[^"]+)"+""",
    """destinationServiceName =({app}[^=]+?)\s*\w+=""",
    """"Location"+:"+(-|({country_code}[^,]+)),""",
    """"(U|u)ser":"(\s|\sAnonymous|({full_name}[^"]+?))\s*"""",
    """"ActivityType"+:"+({operation}[^"]+)"""",
    """"Activity"+:"+({operation}[^"]+)"""",
    """"Path"+:"({uri_path}[^"]+)""",
    """"AdditionalInfo"+:"({additional_info}[^"]+)""",
    """"Action":"({action}[^"]+)""",
    """"Company":"(\\|({company}[^"]+?))\s*"""",
  ]
  ParserVersion = "v1.0.0"


}
```