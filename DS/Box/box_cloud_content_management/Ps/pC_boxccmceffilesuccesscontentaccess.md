#### Parser Content
```Java
{
Name = "box-ccm-cef-file-success-contentaccess"
Vendor = "Box"
Product = "Box Cloud Content Management"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
Conditions = [
"""destinationServiceName =Box"""
"""fname="""
"""msg="""
""""event_type":"CONTENT_ACCESS""""
]
Fields = [
"""([^\|]+\|){5}({access_type}[^\|]+)\|"""
"""([^\|]+\|){5}resource\-({access_type}[^\|]+)\|"""
""""created_at":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)"""
"""\sfname=({file_name}.+?(\.({file_ext}[^\.]+?))?)(\s+\w+=|\s*$)"""
"""\sproto=({file_ext}\w+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""+created_by"+:\{.+?"+name"+:"+(UnknownUser|({full_name}[^\"]+))"+"""
""""+additional_details"+:\{"+size"+:({bytes}\d+)"""
"""\ssuser=({user}[^\s]+?)\s+(\w+=|$)"""
"""\ssuser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)"""
"""\sfileType=({file_type}\w+)"""
""""+parent"+:\{.+?"+name"+:"+({file_dir}[^"]+)"""
""""+event_type"+:"+({access}[^"]+)"+"""
"""(\||\s)requestClientApplication=({app}.+?)(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```