#### Parser Content
```Java
{
Name = "imanage-i-kv-alert-trigger-success-docnum"
Vendor = "iManage"
Product = "iManage"
TimeFormat = "yyyy-MM-dd HH:mm:ss.S"
Conditions = [
"""DOCNUM:"""
"""DOCUSER:"""
]
Fields = [
""""\s*DOCNUM:\s*\"+({file_name}[^\"\s]+)\"+"""
""""\s*ACTIVITY:\s*\"+({alert_type}[^\"\s]+)\"+"""
""""\s*ACTIVITY_DATETIME:\s*\"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d\.\d)"""
""""\s*DOCUSER:\s*\"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\"+"""
""""\s*APPNAME:\s*\"+({app}[^\":]+)\"+"""
""""\s*LOCATION:\s*\"+({host}[^\":]+)\"+"""
]
ParserVersion = "v1.0.0"


}
```