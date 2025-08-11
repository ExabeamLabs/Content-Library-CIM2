#### Parser Content
```Java
{
Name = citrix-sharefile-sk4-app-activity-success-usermodifiedpermission
TimeFormat = [ "MM/dd/yyyy hh:mm:ss a", "M/dd/yyyy hh:mm:ss a", "M/d/yyyy h:mm:ss a", "M/dd/yyyy h:mm:ss a" ]
Conditions = [
  """destinationServiceName =Citrix ShareFile"""
  """"ActivityType":"""
  """"ActionDetails":"""
]
ParserVersion = "v1.0.0"

citrix-app-activity = {
    Vendor = Progress
    Product =  Progress ShareFile
    Fields = [
      """"Date"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
      """"UserMakingChangeEmailAddress":"({email_address}[^@"]+@({email_domain}[^@\."]+\.[^"]+))"""",
      """"Email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
      """"IPAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
      """"+EventID"+:"+({event_code}[^"]+)"+""",
      """({app}Citrix ShareFile)""",
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