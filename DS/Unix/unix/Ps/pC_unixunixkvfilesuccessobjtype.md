#### Parser Content
```Java
{
Name = "unix-unix-kv-file-success-objtype"
Vendor = "Unix"
Product = "Unix"
TimeFormat = "epoch_sec"
Conditions = [
""" Original Address="""
""" objtype="""
""" name="""
]
Fields = [
"""\d\d:\d\d:\d\d ({host}\S+)"""
"""Original Address=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""node=({host}\S+)"""
"""msg=audit\(({time}\d{10})\.\d{3}:\d{10}\):"""
"""\stype=({operation_type}[^=]+?)\s*\w+="""
"""objtype=({action}[^=]+?)\s*\w+="""
"""name="+({file_path}({file_dir}(?:[^";]+)?[\\\/;])?({file_name}[^\\\/";]+(\.({file_ext}[^\\\/\.;"]+))))"""
]
DupFields = [
"operation->action"
]
ParserVersion = "v1.0.0"


}
```