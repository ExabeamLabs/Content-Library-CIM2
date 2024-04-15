#### Parser Content
```Java
{
Name = "github-g-json-app-activity-success-namespaceid"
Vendor = "GitHub"
Product = "GitHub"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""","action":""""
""","remote_ip":""""
""""key":"namespace_id",""""
]
Fields = [
"""time":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)"""
""""action":"({operation}[^"]+)"""
""""remote_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""username":"({user}[^"]+)"""
""""status":({result}[^,"]+)"""
""""path":"({additional_info}[^"]+)"""
""""user_id":({user_id}[^,"]+)"""
""""key":"project_id".+?"value":"({object}[^"]+)"""
""""target_branch":"({object}[^"]+)"""
""""source_branch":"({object}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```