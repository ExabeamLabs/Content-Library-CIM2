#### Parser Content
```Java
{
Name = "xerox-x-kv-printer-activity-success-colorduplexcount"
Vendor = "Xerox"
Product = "Xerox"
TimeFormat = "yyyy-MM-dd HH:mm:ss.s"
Conditions = [
"""account_id: """
"""printer_type: """
"""mono_duplex_count"""
"""color_duplex_count"""
]
Fields = [
"""id:\s*\"+({printer_id}\d+)\"+\s*account_id"""
"""printed:\s*\"+({time}[^\"]+)\""""
"""printer_type:\s*\"+({printer_type}\d+)\"+"""
"""printer_name:\s*\"+({printer_name}[^\"]+)\"+"""
"""object_id:\s*\"+({object_id}({object}\d+))\"+"""
"""user_name:\s*\"+(({domain}[^\"\\]+)\\)?({user}[^\"]+)\"+"""
"""source_machine:\s*\"+({src_host}[^\"]+)\"+"""
"""total_pages:\s*\"+({num_pages}\d+)\"+"""
"""ip_address:\s*\"+0*({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))\"+"""
"""department_name:\s*\"+({department}[^\"]+)\"+"""
"""full_name:\s*\"+({full_name}[^\"]+)\"+"""
"""document_title:\s*\"+({document_name}({object}[^\"]+))\"+"""
]
ParserVersion = "v1.0.0"


}
```