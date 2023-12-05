#### Parser Content
```Java
{
Name = hp-arubaos-str-port-block-00329
  ParserVersion = v1.0.0
  Product = ArubaOS
  Conditions = [ """ 00329 """, """ FFI:""" ]
},  

${DLArubaParsersTemplates.aruba-switch-info}{
  Name = hp-arubaos-str-port-enable-00076
  ParserVersion = v1.0.0
  Product = ArubaOS
  Conditions = [ """ 00076 """, """ ports:""" ]
},  

${DLArubaParsersTemplates.aruba-switch-info}{
  Name = hp-arubaos-str-endpoint-notification-success-00828
  ParserVersion = v1.0.0
  Product = ArubaOS
  Conditions = [ """ 00828 """, """ lldp:""" ]


}
```