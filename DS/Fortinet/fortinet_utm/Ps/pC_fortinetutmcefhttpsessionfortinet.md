#### Parser Content
```Java
{
Name = "fortinet-utm-cef-http-session-fortinet"
Vendor = "Fortinet"
Product = "Fortinet UTM"
TimeFormat = "yyyy-MM-dd 'time='HH:mm:ss"
Conditions = [
"""CEF:0|Fortinet|Fortigate|"""
"""|utm: webfilter|"""
"""url\="""
]
Fields = [
"""\Wdate\\=({time}\d\d\d\d-\d\d-\d\d time\\?=\d\d:\d\d:\d\d([+-]\d\d:\d\d)?)"""
"""\Wdevname\\="*({host}[^\s"]+)"*(\s|")"""
"""\Waction\\="*({action}[^\s"]+)"*(\s|")"""
"""\Wstatus\\="*({action}[^"]+)""""
"""\Wurl\\="*(?:-|\w+:\/+[^\/]+)?({uri_path}\/[^?\s"]*)"""
"""\Wurl\\="*(?:[^?]+?(|({uri_query}\?[^\s"]+)))["\s]*(\w+\\=|$)"""
"""\Wcatdesc\\="*({category}[^"]+?)["\s]*(\w+\\=|$|,)"""
"""\Wuser\\="*({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""\Wsrcip\\*="*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wdstip\\*="*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""\Whostname\\="*({web_domain}[^"\s]+)"""
"""\Wservice\\="*({protocol}[^\s"]+)"*(\s|")"""
"""\Wlevel\\="*({alert_severity}[^\s"]+)"*(\s|")"""
"""\Wdstport\\=({dest_port}\d+)(\s|")"""
"""\Wsentbyte\\=({bytes_out}\d+)(\s|")"""
"""\Wrcvdbyte\\=({bytes_in}\d+)(\s|")"""
"""\Wdevid\\="*({asset_id}[^"\s]+)"*(\s|")"""
"""\Wreferralurl\\="*({referrer}[^"\s]+)"""
"""\Wgroup\\="*({user_group_name}.+?)["\s]*(\w+\\=|$)"""
"""\Wmsg\\="*({additional_info}.+?)["\s]*(\w+\\=|$)"""
"""\Waction\\="*blocked"*.+?\Wmsg\\="*({result_reason}.+?)["\s]*(\w+\\=|$)"""
"""\Wmsg\\="*({result_reason}.+?)["\s]*(\w+\\=|$).+?\Waction\\="*blocked"*""",
"""\Wtz="?({tz}[+-]\d+)"""
]
ParserVersion = "v1.0.0"


}
```