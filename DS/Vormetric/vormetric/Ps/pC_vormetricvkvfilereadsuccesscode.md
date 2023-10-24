#### Parser Content
```Java
{
Name = "vormetric-v-kv-file-read-success-code"
Vendor = "Vormetric"
Product = "Vormetric"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [
""" gp="""
""" denyStr=""""
""" uinfo=""""
""" showStr=""""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\S+\s+({dest_host}[\w.\-]+)"""
"""\suinfo=\"({user}[\w\.\-]{1,40}\$?)\\+[^\"]+?({domain}[^,\"\\]+?),[^,\"\\]*?\""""
"""\ssproc=\"({process_path}({process_dir}[^\"]*?)(\\+({process_name}[^\"\\]+?))?)\""""
"""\sact=\"({access}[^\"]+)\""""
"""\sgp=\"({file_dir}[^\"]+)\""""
"""\sfilePath=\"\\+({file_name}[^\"\\]+)\""""
"""\sdenyStr=\"({action}[^\"]+)\""""
"""({alert_name}DENIED)"""
]
ParserVersion = "v1.0.0"


}
```