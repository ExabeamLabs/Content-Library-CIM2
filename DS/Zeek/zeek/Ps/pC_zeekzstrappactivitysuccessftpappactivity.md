#### Parser Content
```Java
{
Name = "zeek-z-str-app-activity-success-ftpappactivity"
Vendor = "Zeek"
Product = "Zeek"
TimeFormat = "epoch_sec"
Conditions = [
"""<Bro FTP App Activity Conditions>"""
]
Fields = [
""".*?({time}\d{10})\.\d{6}"""
"""([^\t]+\t){2}(({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({src_host}[^\t]+))\t({src_port}\d+)"""
"""([^\t]+\t){4}(({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))|({dest_host}[^\t]+))\t({dest_port}\d+)"""
"""\t21\t(?:<unknown>|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
"""\t21\t([^\t]+\t){2}({operation}[^\t]+)"""
"""({app}ftp)"""
"""\t21\t([^\t]+\t){3}ftp:(\/)+.*?\/({object}[^\/\t]+)\t(?:-|<unknown>|({mime}[^\s]+))"""
"""\t21\t([^\t]+\t){7}(?:-|({additional_info}[^\(\t]+))"""
]
ParserVersion = "v1.0.0"


}
```