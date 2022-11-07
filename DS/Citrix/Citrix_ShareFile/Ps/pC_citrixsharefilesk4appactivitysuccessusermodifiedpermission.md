#### Parser Content
```Java
{
Name = citrix-sharefile-sk4-app-activity-success-usermodifiedpermission
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """destinationServiceName =Citrix ShareFile"""
  """"ActivityType":"""
  """"ActionDetails":"""
]
ParserVersion = "v1.0.0"

citrix-app-activity = {
    Vendor = Citrix
    Product =  Citrix ShareFile
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
    
}
```