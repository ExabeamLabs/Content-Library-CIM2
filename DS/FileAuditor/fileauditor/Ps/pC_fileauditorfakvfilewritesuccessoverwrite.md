#### Parser Content
```Java
{
Name = fileauditor-fa-kv-file-write-success-overwrite
  ParserVersion = "v1.0.0"
  Conditions = [ """[ FILE_ATTRIBUTES=""", """[ CREATION_TIME=""", """[ MESSAGE=Overwrite ]""" ]

fileauditor-file-operations = {
  Vendor = FileAuditor
  Product = FileAuditor
  TimeFormat = "epoch_sec"
  Fields = [
    """\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+\-]\d\d:\d\d\s+({host}[\w\-.]+)"""
    """\[ CREATION_TIME=({time}\d{10})"""
    """\[ OLD_SHARE_PATH=({src_file_dir}[^\]]+\\+)?({src_file_name}[^\]\\\/]+?)\s*\]"""
    """\[ NEW_FILE_NAME=({file_path}({file_dir}[^\]]*?)[\\\/]*({file_name}[^\\\]]+?(\.({file_ext}[^\.\s\]]+))?))\s*\]"""
    """\[ CLIENT_HOST=(-|(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-.]+)))"""
    """\[ CLIENT_IP=(::1|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
    """\[ MESSAGE=({access}.+?)\s*\]"""
    """\[ USERNAME=({user}[^\s\]]+?)\s*\]"""
   ]
  DupFields = [ "host->dest_host" 
}
```