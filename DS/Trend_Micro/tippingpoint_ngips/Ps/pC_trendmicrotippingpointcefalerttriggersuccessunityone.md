#### Parser Content
```Java
{
Name = "trendmicro-tippingpoint-cef-alert-trigger-success-unityone"
Vendor = "Trend Micro"
Product = "TippingPoint NGIPS"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|TippingPoint|UnityOne|"""
"""app="""
]
Fields = [
"""\Wdvchost=({host}\S+)\s*(\w+=|$)"""
"""\Wrt=({time}\d{13})"""
"""CEF:([^\|]*\|){4}({alert_type}[^\|]+)\|(?:\d+:\s*)?({alert_name}[^\|]+)\|({alert_severity}\d+)"""
"""\Wdhost=({dest_host}[\w\-\.]).*?\s*(\w+=|$)"""
"""\Wsrc=(0\.0\.0\.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""\Wdst=(0\.0\.0\.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\sdpt=({dest_port}\d+)"""
"""\sspt=({src_port}\d+)"""
"""\sproto=({protocol}[^\s]+)"""
"""\scat=({additional_info}[^=]+?)\s*\w+="""
"""app=({app}[^=]+?)\s*\w+="""
"""\sact=({action}[^=\s]+?)\s*\w+="""
]
ParserVersion = "v1.0.0"


}
```