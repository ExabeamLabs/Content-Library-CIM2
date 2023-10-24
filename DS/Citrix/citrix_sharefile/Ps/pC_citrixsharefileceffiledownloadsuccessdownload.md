#### Parser Content
```Java
{
Name = "citrix-sharefile-cef-file-download-success-download"
Vendor = "Citrix"
Product = "Citrix ShareFile"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
"""destinationServiceName =Citrix ShareFile"""
""""Activity":"Download""""
""""Email":""""
]
Fields = [
""""Date"+:"+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""Email":"({email_address}[^@"]+@({email_domain}[^@"]+))""""
""""IPAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""+EventID"+:"+({event_code}[^"]+)"+"""
"""destinationServiceName =({app}[^=]+?)\s*\w+="""
""""Location"+:"+(-|({country_code}[^,]+)),"""
""""(U|u)ser":"(\s|\sAnonymous|({full_name}[^"]+?))\s*""""
""""ActivityType"+:"+({operation}[^"]+)""""
""""Activity"+:"+({operation}[^"]+)""""
""""Path"+:"({uri_path}[^"]+)"""
""""AdditionalInfo"+:"({additional_info}[^"]+)"""
""""Action":"({action}[^"]+)"""
""""Company":"(\\|({company}[^"]+?))\s*""""
""""ItemName"+:"+({file_path}({file_dir}[^"]*[\/]+)\s*({file_name}[^\/"]+(\.({file_ext}[^\/"]+))))""""
]
DupFields = [ "file_name->src_file_name" , "file_ext->src_file_ext" , "file_path->src_file_path"]
ParserVersion = v1.0.0


}
```