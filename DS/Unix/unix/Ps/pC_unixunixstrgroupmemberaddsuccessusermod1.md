#### Parser Content
```Java
{
Name = "unix-unix-str-group-member-add-success-usermod-1"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
Conditions = [
"""]["""
""" usermod """
""" add """
""" group """
]
Fields = [
"""\[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]\[\d+\]\["""
"""<\d+>\d+ ({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d) ({host}[\w.\-]+) usermod"""
"""add '({account_name}[^']+)' to.+?group '({group_name}[^']+)'"""
"""\s+({process_name}\S+)\[({process_id}\d+)\]\:\s*"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```