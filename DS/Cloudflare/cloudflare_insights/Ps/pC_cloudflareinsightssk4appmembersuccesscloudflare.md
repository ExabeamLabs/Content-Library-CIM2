#### Parser Content
```Java
{
Name = "cloudflare-insights-sk4-app-member-success-cloudflare"
Vendor = "Cloudflare"
Product = "Cloudflare Insights"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ","yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Conditions = [
"""CEF:"""
"""destinationServiceName =cloudflare"""
""""when":""""
]
Fields = [
""""when":"({time}[^"]+)""""
""""ip":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
""""action":[^\$]+?"type":"({operation}[^",]+)""""
""""actor":\{"email":"({email_address}[^@"]+@[^\."]+\.[^"]+)"""",
"""suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""destinationServicename=({app}[^\s]+)"""
"""flexString1=({operation}[^\s]+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""msg=({additional_info}.+?)\s\w+="""
""""account_name":"({account_name}[^"]+)"""",
""""user_email":"({account}[^"]+)"""",
""""resource":[^\$]+?"type":"({object_type}[^,"]+)"""",
""""resource":[^\$]+?"id":"({object_id}[^,"]+)"""",
""""action":[^\$]+?"result":({result}[^,"]+)""",
]
ParserVersion = "v1.0.0"


}
```