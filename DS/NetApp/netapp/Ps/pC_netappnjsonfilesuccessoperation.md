#### Parser Content
```Java
{
Name = "netapp-n-json-file-success-operation"
ParserVersion = "v1.0.0"
Vendor = "NetApp"
Product = "NetApp"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""timestamp""""
""""volumeName"""
""""netapp"""
""""entityAccessedTime"""
""""activityType"""
]
Fields = [
""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,9}Z)"""
""""hostname":"({host}[^"]+)""""
""""userDisplayName\\*":\\*"({full_name}[^"]+?)\\*""""
""""entityType\\*":\\*"({file_type}[^"]+?)\\*""""
""""userName\\*":\\*"({user}[\w\.\-\!\#\^\~]{1,40}\$?)\\*""""
""""domain\\*":\\*"({domain}[^"]+?)\\*""""
""""extension\\*":\\*"({file_ext}[^"]+?)\\*""""
""""entityName\\*":\\*"({file_name}[^"]+?)\\*""""
""""entityPath\\*":\\*"({file_path}({file_dir}[^"]*?)[\\\/]*[^\/"]+?)\\*""""
""""activityType\\*":\\*"({access}[^"]+?)\\*""""
""""host\\*":\\*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\\*""""
]
DupFields = [
"access->operation"
]


}
```