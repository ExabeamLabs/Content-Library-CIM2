#### Parser Content
```Java
{
Name = "symantec-wss-kv-http-session-filter"
Vendor = "Symantec"
Product = "Symantec Web Security Service"
TimeFormat = ["dd/MM/yyyy:HH:mm:ss z","dd/MM/yyyy:HH:mm:ss Z", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
Conditions = [
"""filter-result="""
"""cs-host="""
]
Fields = [
"""\tcs-userdn=(?:-|(({domain}[^\\\t]+)\\)?({user}[\w\.\-]{1,40}\$?))"""
"""\Ws-ip="?(-|({host}[\w\-.]+?))("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Ws-computername="?(-|({host}[^"|]))("|\||$|\t|\s+[\w\-\(\)]+=)"""
""""@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""""
""""timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)""""
"""date="?({time}\d\d\d\d-\d\d-\d\d"?(,|\t|\s)time="?\d\d:\d\d:\d\d)"""
"""\Wdevicetime=\[({time}\d+\/\d+\/\d+:\s*\d+:\d+:\d+ [^\]]+)"""
"""date="({time}\d\d\/\d\d\/\d\d\d\d:\s\d\d:\d\d:\d\d[^"]+)""""
"""\W(c-ip|src)="?(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""\tr-ip=(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\Wsrcport=(-|({src_port}\d+))"""
"""\Wdst=(-|({external_dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))"""
"""\Wdstport=(?:-|({dest_port}\d+))"""
"""\W(cs-username|username)="?(-|({user}[\w\.\-]{1,40}\$?))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Ws-action="?(-|({proxy_action}[^"|]+))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\W(sc|cs)-status="?(-|({http_response_code}\d+))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Wcs-method="?((?i)(unknown)|-|({method}[^"|]+))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\W(sc|rs)-bytes="?(-|({bytes_out}\d+))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Wcs-bytes="?(-|({bytes_in}\d+))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Wcs-uri-scheme="?(-|({protocol}[^"|]+))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Wcs-host="?(-|({web_domain}[a-zA-z0-9.\-_]+(\.[a-zA-Z]{2,})?))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Wcs-uri="?(-|({url}[^"|]+))\s*(?:"|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Wcs-uri-path="?(\/|-|({uri_path}[^"|]+))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Wcs-uri-query="?(-|({uri_query}[^"|]+))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Wcs-uri-extension="?(-|({mime}[^;"|]+))\s*("|\||$|\t|;|\s+[\w\-\(\)]+=)"""
"""\Wrs\(\s?Content\-Type\)="?(-|({mime}[^;"|]+))\s*("|\||$|\t|;|\s+[\w\-\(\)]+=)"""
"""\Wcs\(User-Agent\)="?(-|({user_agent}[^"|]+))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\W(sc-)?filter-result="?(-|({action}[^"|]+))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\W(sc-)?filter-category="?((?i)none|-|({category}[^"|]+))\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Wcs-categories="?((?i)none|-|({categories}({category}[^"|;]+)[^"|]*))"?\s*("|\||$|\t|;|\s+[\w\-\(\)]+=)"""
"""\Wcs-categories="?((?i)none|-|({categories}({category}[^;"]+)[^"|]*))"?\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Wcs\(Referer\)"?=("?-"?|"?({referrer}[^"\|\t]+?)"?)\s*("|\||$|\t|\s+[\w\-\(\)]+=)"""
"""\Wreference_id="*(-|({reference_id}[^"]+))"*"""
]
DupFields = [
"external_dest_ip->dest_ip"
]
ParserVersion = "v1.0.0"


}
```