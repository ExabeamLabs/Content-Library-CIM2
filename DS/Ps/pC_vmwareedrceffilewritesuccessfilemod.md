#### Parser Content
```Java
{
Name = "vmware-edr-cef-file-write-success-filemod"
   ParserVersion = v1.0.0
   Conditions = [ """"type":"endpoint.event.filemod"""", """"process_username":"""", """"event_origin":"EDR"""" ]
   Fields = ${CarbonBlackParsersTemplates.carbonblack-edr.Fields}[
    """parent_path":"({parent_process_path}({parent_process_dir}[^"]+(\\|\/)+)?({parent_process_name}[^"]+))"""
   ]


}
```