#### Parser Content
```Java
{
Name = "crowdstrike-falcon-mix-file-write-success-directorycreate"
ParserVersion = "v1.0.0"
Vendor = "CrowdStrike"
Product = "Falcon"
TimeFormat = "epoch_sec"
Conditions = [
""""event_simpleName":"""
""""DirectoryCreate""""
]
Fields = [
"""\"timestamp\":\s*\"({time}\d{10})"""
"""\"event_simpleName\":\s*\"({event_code}[^\"]+)"""
"""\"aid\":\s*\"({aid}[^\"]+)"""
"""\"TargetFileName\":\s*\"({file_path}[^\"]+)"""
""""TargetFileName":"({file_path}(({file_dir}[^"]*?)[\\\/]+)?\s*({file_name}[^\\\/"]+?(\.(\d+|({file_ext}[^\\\/"\.]+)))?))"""",
"""({file_type}Directory)"""
"""suser=(system|({user}[\w\.\-]{1,40}\$?))"""
"""src-account-name\":\"({account_name}[^\"]+)""",
""""aip":\s*"({aip}[^"]+)"""",
""""ShareAccess":"({access}[^"]+)"""",
""""cid":"({cid}[^"]{1,2000})"""
""""event_platform":"({os}[^"]+)""""
]


}
```