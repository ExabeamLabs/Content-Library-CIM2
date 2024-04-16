#### Parser Content
```Java
{
Name = "zscaler-ia-kv-http-session-https"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = "yyyy-MM-ddHH:mm:ss"
Conditions = [
"""dlpidentifier="""
"""dlpdictionaries="""
"""dlpengine="""
"""url="""
"""appclass="""
"""appname="""
"""clientpublicIP="""
"""refererURL="""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\d\d\d:\d+:\d+)\s+(\w+=|$)"""
"""urlcategory=(Miscellaneous or Unknown|({category}[^=]+?))\s+(\w+=|$)"""
"""\saction=({action}[^=]+?)\s*(\w+=|$)"""
"""\sprotocol=({protocol}[^=]+?)\s*(\w+=|$)"""
"""\sserverip=(?:0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\srequestmethod=(NA|({method}[^=]+?))\s*(\w+=|$)"""
"""\srefererURL="*(?:None|({referrer}[^\s]+?))\/?"*\s*(\w+=|$)"""
"""\suseragent=(Unknown|({user_agent}[^=]+?))\s*(\w+=|$)"""
"""\sstatus=({http_response_code}\d+)"""
"""\sclientpublicIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sClientIP=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\suser=((({domain}[\w.\-]+)->[^=]+?)|({email_address}[^@]+@[^\s=]+?))(\s+\w+=|\s*$)"""
"""\surl="*(?:None|({url}[^\s"]+))"*\s*(\w+=|$)"""
"""\surl="*(\w+:\/{2})?[^\/]+({uri_path}\/[^?\s"]+)"""
"""\surl="*[^=|?]+({uri_query}\?[^\s"]+)"?\s"""
"""\shostname=(\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|({web_domain}\S+))"""
"""\sappname=\s*({app}[^=]+?)\s+(\w+=|$)"""
"""\suser=(?![^\s]+@[^\s]+)({user}[\w\.\-]{1,40}\$?)\s*(\w+=|$)"""
"""\srefererURL=(?:None|({referrer}[^\s]+))\s*(\w+=|$)"""
"""\scontenttype=(?:None|({mime}[^=]+?))\s*(\w+=|$)""",
"""\slocation=({location}[^=]+?)\s+\w+="""
"""\surlcategory=({categories}({category}[^;,=]+)[^=]*?)\s+(\w+|$)"""
]
ParserVersion = "v1.0.0"


}
```