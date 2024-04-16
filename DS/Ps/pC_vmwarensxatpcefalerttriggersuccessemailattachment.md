#### Parser Content
```Java
{
Name = "vmware-nsxatp-cef-alert-trigger-success-emailattachment"
Conditions = [
"""CEF:"""
"""|Lastline|"""
"""|email-attachment|"""
"""|Suspicious Email Attachment|"""
]
ParserVersion = "v1.0.0"

carbonblack-edr.Fields}[
    """parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))"""
   
}
```