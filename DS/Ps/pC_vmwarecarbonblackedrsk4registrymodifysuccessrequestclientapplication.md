#### Parser Content
```Java
{
Name = vmware-carbonblackedr-sk4-registry-modify-success-requestclientapplication
  Conditions = [ """"type":"endpoint.event.regmod"""", """"process_username":"""", """"event_origin":"EDR"""" ]
  Fields = ${DLCarbonBlackParsersTemplates.carbonblack-edr.Fields} [
    """"regmod_name":"({registry_path}[^"]+(\\|\/)+?({registry_key}[^"]+))""""
    ]
  ParserVersion = "v1.0.0"


}
```