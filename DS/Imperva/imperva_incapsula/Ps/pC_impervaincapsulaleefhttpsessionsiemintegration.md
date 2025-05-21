#### Parser Content
```Java
{
Name = "imperva-incapsula-leef-http-session-siemintegration"
Vendor = "Imperva"
Product = "Imperva Incapsula"
TimeFormat = "epoch"
Conditions = [
"""LEEF:"""
"""|Incapsula|SIEMintegration|"""
"""deviceExternalId="""
"""fileId="""
]
Fields = [
"""\d:\d\d:\d\d\.\d+Z\s({host}[^\s]+)"""
"""\Wstart=({time}\d{13})"""
"""siteid=({site_id}\d+)"""
"""requestMethod=({method}[^\s]+)"""
"""\WsourceServiceName =({web_domain}.+?)\s+(\w+=|$)"""
"""\WrequestClientApplication=({user_agent}[^=]+?)\s+(\w+=|$)"""
"""ref=({referrer}[^\s]+)"""
"""proto=({protocol}[^\s]+)"""
"""srcPort=({src_port}\d+)"""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdproc=({category}[^=]+?)\s+(\w+=|$)"""
"""calCountryOrRegion=({country_code}[^\s]+)"""
"""\Wurl=(-|({url}(({protocol}[^:\\\/\s]+):[\\\/]+)?({web_domain}[^\\\/\s:]+)(:\d+)?(\/|({uri_path}\/[^\?"]*?))?({uri_query}\?[^"\s]*?)?))\s+(\w+=|$)"""
"""cat=({action}[^\s]+)"""
"""dstPort=({dest_port}\d+)"""
"""dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""cs9=(,)?(,|\s+|({alert_name}[^=]+?))\s*(,|\w+=|$)"""
"""LEEF[^|]+\|([^|]*\|){3}({categories}[^|]+)"""
"""cs6=({app}[^=]+?)\s+(\w+=|$)"""
"""fileId=({alert_id}\d+)"""
"""cn1=({http_response_code}\d+)"""
"""qstr=({uri_query}[^\s]+)"""
]
ParserVersion = "v1.0.0"


}
```