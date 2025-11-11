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
"""\suinfo=\"({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\\+[^\"]*?({domain}[^,\"\\]+))?"""
"""\ssproc=\"({process_path}({process_dir}[^\"]*?)(\\+({process_name}[^\"\\]+?))?)\""""
"""\sact=\"({access}[^\"]+)\""""
"""\sgp=\"({file_dir}[^\"]+)\""""
"""\sfilePath=\"\\+({file_name}[^\"\\]+?(\.({file_ext}[^\.\s"\\]+?))?)\""""
"""\sdenyStr=\"({action}[^\"]+)\""""
"""({alert_name}DENIED)"""
"""\spol=\"({policy_name}[^\"]+)\""""
"""\suid=({user_id}\d+)"""
"""\sgid=({group_id}\d+)\\\+({group_name}[^\\]+)"""
"""\suinfo=\"({user_info}[^"]+)"""
"""\skey=\"({key_name}[^\"]+)\""""
]
ParserVersion = "v1.0.0"


}
```