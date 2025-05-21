#### Parser Content
```Java
{
Name = "forcepoint-wsg-kv-http-session-apiexportcsvtokv"
Vendor = "Forcepoint"
Product = "Websense Security Gateway"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""logtype="ForcepointAPIExportCSVtoKV""""
"""Referrer_URL_-_Full=""""
"""HTTP_Status_Code="""
]
Fields = [
"""Action="(?:-|({action}[^"]+))"""
"""Bytes_Sent="({bytes_out}\d+)""""
"""Bytes_Received="({bytes_in}\d+)""""
"""Category_Name ="(Unknown|({category}[^"]+))""""
"""Destination_IP="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
"""Source_IP="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
"""\sURL_-_Full="({url}({protocol}[^:]+):\/\/({web_domain}[^\/:\s]+))?({uri_path}\/?[^\?"]+)?(\?({uri_query}[^"]+))?""""
"""Referrer_URL_-_Full="((?i)None|({referrer}[^"]+))"""
"""Workstation="(Not available|({host}[^"]+))""""
"""Request_Method="({method}[^"]+)""""
"""Full_MIME_Type="(None|({mime}[^"]+))""""
"""User_Agent="(None|({user_agent}[^"]+))""""
"""HTTP_Status_Code="({http_response_code}\d+)""""
"""Workstation="(Not available|({src_host}[^"]+))""""
"""User="(Not available|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
"""File_Name ="((?i)none|({file_name}[^"]+))""""
"""File_Type="((?i)Unknown|({file_type}[^"]+))"""
]
ParserVersion = "v1.0.0"


}
```