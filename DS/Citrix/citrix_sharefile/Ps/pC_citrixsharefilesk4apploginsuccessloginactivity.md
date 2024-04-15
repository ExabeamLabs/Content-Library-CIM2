#### Parser Content
```Java
{
Name = "citrix-sharefile-sk4-app-login-success-loginactivity"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""destinationServiceName =Citrix ShareFile"""
""""Activity":"Login""""
""""Email":"""
]
ParserVersion = "v1.0.0"

citrix-app-activity = {
    Vendor = Citrix
    Product =  Citrix ShareFile
    Fields = [
      """"Date"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"UserMakingChangeEmailAddress":"({email_address}[^@"]+@({email_domain}[^@\."]+\.[^"]+))"""",
      """"Email":"({email_address}[^@"]+@({email_domain}[^@"]+))"""",
      """"IPAddress"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"+EventID"+:"+({event_code}[^"]+)"+""",
      """destinationServiceName =({app}[^=]+?)\s*\w+=""",
      """"Location"+:"+(-\s*|({country_code}[^,]+)),""",
      """"(U|u)ser":"\s*(\s|\sAnonymous|({full_name}[^"]+?))\s*"""",
      """"ActivityType"+:"+({operation}[^"]+)"""",
      """"Activity"+:"+({operation}[^"]+)"""",
      """"Path"+:"({uri_path}[^"]+)""",
      """"AdditionalInfo"+:"({additional_info}[^"]+)""",
      """"Action":"({action}[^"]+)""",
      """"Company":"\s*(\\|({company}[^"]+?))\s*"""",
    
}
```