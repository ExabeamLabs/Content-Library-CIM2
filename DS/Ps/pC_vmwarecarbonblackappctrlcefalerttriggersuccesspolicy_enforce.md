#### Parser Content
```Java
{
Name = "vmware-carbonblackappctrl-cef-alert-trigger-success-policy_enforce"
Conditions = [
"""CEF:"""
"""|VMware Carbon Black|App Control|"""
"""cat="""
"""externalId="""
]
ParserVersion = "v1.0.0"

carbonblack-edr.Fields}[
    """"parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))""""
}
```