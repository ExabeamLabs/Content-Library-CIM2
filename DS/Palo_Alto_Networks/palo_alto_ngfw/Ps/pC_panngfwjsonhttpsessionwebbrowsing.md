#### Parser Content
```Java
{
Name = "pan-ngfw-json-http-session-webbrowsing"
Vendor = "Palo Alto Networks"
Product = "Palo Alto NGFW"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
""""LogType":"THREAT""""
""""HTTPMethod":"""
""""URL":"""
""""Subtype":"url""""
""""Application":"web-browsing""""
]
Fields = [
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""""
""""host":"({host}[^"]+)""""
""""SourceUser":"({email_address}[^\@]+\@[^"]+)""""
""""SourceAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""SourcePort":({src_port}\d+),""""
""""DestinationAddress":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
""""DestinationPort":({dest_port}\d+),""""
""""HTTPMethod":"({method}[^"]+)""""
""""Action":"({action}[^"]+)""""
""""URL":"({url}({web_domain}[^"\/\?]+)({uri_path}\/[^?"]*)?({uri_query}\?[^"]+)?)"""
""""Referer":"({referrer}[^"]+)""""
""""Protocol":"({protocol}[^"]+)""""
""""UserAgent":"({user_agent}[^"]+?)\s*""""
""""URLCategoryList":"({categories}[^"]+)""""
""""URLCategory":"({category}[^"]+)""""
""""ContentType":"({mime}[^"]+)""""
""""DirectionOfAttack":"({direction}[^"]+)""""
]
ParserVersion = "v1.0.0"


}
```