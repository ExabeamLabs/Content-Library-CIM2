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
    """"Email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """"IPAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
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