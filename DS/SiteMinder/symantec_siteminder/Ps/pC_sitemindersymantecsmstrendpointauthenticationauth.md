#### Parser Content
```Java
{
Name = "siteminder-symantecsm-str-endpoint-authentication-auth"
Vendor = "SiteMinder"
Product = "Symantec SiteMinder"
TimeFormat = "MMM dd',' yyyy',' HH:mm:ss a"
Conditions = [
""""CA SiteMinder@""""
"""Authentication"""
]
Fields = [
""""({auth_type}[^"]+?)","CA SiteMinder@"""
""""CA SiteMinder@.*?",("[^"]+?",){1}"({time}\w+ \d+, \d\d\d\d, \d+:\d+:\d+ (AM|PM|am|pm))""""
""""CA SiteMinder@.*?",("[^"]+?",){2}"({result}[^"]+?)""""
""""CA SiteMinder@.*?",("[^"]+?",){3}"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""CA SiteMinder@.*?",("[^"]+?",){5}"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""CA SiteMinder@.*?",("[^"]+?",){7}"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
]
ParserVersion = "v1.0.0"


}
```