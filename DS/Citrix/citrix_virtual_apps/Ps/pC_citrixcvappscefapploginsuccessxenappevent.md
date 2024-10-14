#### Parser Content
```Java
{
Name = "citrix-cvapps-cef-app-login-success-xenappevent"
Vendor = "Citrix"
Product = "Citrix Virtual Apps"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Citrix|Cirtix XenApp"""
""" rt="""
]
Fields = [
"""\sdvc=({host}.+?)\s+\w+="""
"""\sdvchost=({host}.+?)\s+\w+="""
"""\scs2=({host}.+?)\s+\w+="""
"""\sshost=({src_host}.+?)\s+\w+="""
"""\srt=({time}\d{13})"""
"""\Wsrc=(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
"""\Wdst=(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""
"""\sexternalId=({alert_id}.+?)\s+\w+="""
"""\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
"""\|Citrix\|({app}[^\|]+)\|"""
"""\ssourceServiceName =({app}.+?)\s+\w+="""
"""\ssuid=({full_name}.+?)\s+\w+="""
"""\scs4=({os}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```