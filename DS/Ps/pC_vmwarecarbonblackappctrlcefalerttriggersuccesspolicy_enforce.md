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
     """exa_json_path=$.parent_path,exa_regex=({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))"""
     """"parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))""""    
  ]
  ParserVersion = v1.0.0
},

${CarbonBlackParsersTemplates.carbonblack-endpoint}{
  Name = "vmware-carbonblackedr-mix-file-filemod"
  ParserVersion = "v1.0.0"
  Conditions = [ """filemod""" , """carbonblack""" , """sensor_action""" 
}
```