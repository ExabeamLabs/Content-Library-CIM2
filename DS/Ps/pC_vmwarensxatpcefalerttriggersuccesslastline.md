#### Parser Content
```Java
{
Name = "vmware-nsxatp-cef-alert-trigger-success-lastline"
Conditions = [
"""CEF:"""
"""|Lastline|"""
"""|dns-resolution|"""
"""|Suspicious DNS Resolution|"""
]
ParserVersion = "v1.0.0"

carbonblack-edr.Fields}[
    """parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))"""
   
}
```