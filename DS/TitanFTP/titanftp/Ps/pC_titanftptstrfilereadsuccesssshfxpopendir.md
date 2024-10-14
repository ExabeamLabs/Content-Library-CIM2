#### Parser Content
```Java
{
Name = "titanftp-t-str-file-read-success-sshfxpopendir"
Vendor = "TitanFTP"
Product = "TitanFTP"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""" COMMAND: """
"""szInPath=""""
"""SFTP->SSH_FXP_OPENDIR"""
]
Fields = [
"""({time}\d+-\d+-\d+\s+\d+:\d+:\d+)\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({dest_port}\d+)\s+\d+\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+({src_port}\d+)\s+\d+\s({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+({bytes}\d+)"""
"""COMMAND:\s*({access}.+?)\s+([\w\-]+=|$)"""
"""szInPath=\"(|({file_path}({file_dir}[^\"]+?)[\\\/]*({file_name}[^\\\/\"]+?(\.({file_ext}[^\\\.\s\"]+))?)?))\""""
]
DupFields = [
"dest_ip->host"
]
ParserVersion = "v1.0.0"


}
```