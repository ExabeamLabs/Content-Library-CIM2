#### Parser Content
```Java
{
Name = "vmware-idm-json-user-privilege-use-success-vidm"
Vendor = "VMware"
Product = "VMware Identity Manager"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS z"
Conditions = [
"""filepath="""
"""vidm"""
"""Thread-"""
"""Originator@"""
]
Fields = [
""""host":"({host}[^\"]+)""""
""""_time":"({time}[^\"]+)""""
""""source":"({log_source}[^\"]+)\""""
""""sourcetype\":\"({source_type}[^\"]+)""""
"""\d+Z\s*({host}[^\s]+)\s"""
"""filepath=\\\"({file_path}[^\"]+)\\\""""
"""Thread-({thread_id}\d+)"""
"""CN=(Not Available|({full_name}\w+(\s+\w+)+)|({user}[\w\.\-]{1,40}\$?)),(?:OU|DC|CN)="""
"""product=\\*\"({app}[^\\\"=:]+)\\*\""""
]
ParserVersion = "v1.0.0"


}
```