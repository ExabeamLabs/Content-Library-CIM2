#### Parser Content
```Java
{
Name = "google-workspace-sk4-file-success-googleapps1"
Vendor = "Google"
Product = "Google Workspace"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
""""name" : "doc_type"""
""""name" : "doc_title""""
""""applicationName" : "drive""""
]
Fields = [
"""([^\|]+\|){5}({access}[^\|]+)\|"""
"""([^\|]+\|){5}resource\-({access}[^\|]+)\|"""
""""time"\s*:\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)"""
"""\sfname=({file_name}.+?(\.({file_ext}[^\.]+?))?)(\s+\w+=|\s*$)"""
"""\sproto=({file_ext}\w+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""+created_by"+:\{.+?"+name"+:"+({full_name}[^"]+)"+"""
""""+additional_details"+:\{"+size"+:({bytes}\d+)"""
"""(\||\s)suser=({email_address}[^"]+?)(\s+\w+=|[\s"]*$)"""
"""(\||\s)sproc=({email_address}[^"]+?)(\s+\w+=|[\s"]*$)"""
"""\sfileType=({file_type}\w+)"""
""""+parent"+:\{.+?"+name"+:"+({file_dir}[^"]+)"""
""""+event_type"+:"+({access}[^"]+)"+"""
"""(\||\s)requestClientApplication=({app}.+?)(\s+\w+=|\s*$)"""
"""filePermission=({access_type}[^\s]+)"""
]
DupFields = [
"email_address->user"
]
ParserVersion = "v1.0.0"


}
```