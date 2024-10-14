#### Parser Content
```Java
{
Name = "zscaler-ia-cef-http-session-mcafeeesm"
Vendor = "Zscaler"
Product = "Zscaler Internet Access"
TimeFormat = "epoch"
Conditions = [
"""|McAfee|ESM|"""
"""ZSCALER"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""\sdeviceTranslatedAddress=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\ssuser=(?![^\s]+@[^\s]+)({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\ssuser=(?=[^\s]+@[^\s]+)({email_address}({user}[\w\.\-\!\#\^\~]{1,40}\$?)@[^\s]+)"""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)@"""
"""\sduser=({browser}.+?)\s+(\(|\w+=)"""
"""\sact=({action}.+?)\s+\w+="""
"""\snitroResponse_Code=({http_response_code}\d+)"""
"""\snitroURL=({url}\S+)"""
"""\snitroURL_Category=({category}.+?)\s+(-|\w+=)"""
"""\snitroURL=(\w+:\/{2})?[^\/]+({uri_path}\/[^?\s]+)"""
"""\snitroURL=[^=|?]+({uri_query}\?[^\s]+)\s"""
"""\snitroURL=(?:[^:?]+:\/+)?({web_domain}[^\/:\s]+)"""
]
ParserVersion = "v1.0.0"


}
```