#### Parser Content
```Java
{
Name = "citrix-sharefile-cef-file-upload-success-fileupload"
Vendor = "Progress"
Product = "Progress ShareFile"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""destinationServiceName =Citrix ShareFile"""
""""Activity":"Upload""""
""""Email":""""
]
Fields = [
""""Date"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""Email":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
""""IPAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""+EventID"+:"+({event_code}[^"]+)"+"""
"""({app}Citrix ShareFile)"""
""""Location"+:"+(-|({country_code}[^,]+)),"""
""""(U|u)ser":"(\s|\sAnonymous|({full_name}[^"]+?))\s*""""
""""ActivityType"+:"+({operation}[^"]+)""""
""""Activity"+:"+({operation}[^"]+)""""
""""Path"+:"({uri_path}[^"]+)"""
""""AdditionalInfo"+:"({additional_info}[^"]+)"""
""""Action":"({action}[^"]+)"""
""""Company":"(\\|({company}[^"]+?))\s*""""
""""ItemName"+:"+({src_file_path}({file_path}({file_dir}[^"]*[\/]+)\s*({src_file_name}({file_name}[^\/"]+(\.({src_file_ext}({file_ext}[^\/"\.\s]+)))))))""""
]
ParserVersion = "v1.0.0"


}
```