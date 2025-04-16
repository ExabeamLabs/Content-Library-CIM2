#### Parser Content
```Java
{
Name = fortinet-fortigate-kv-network-notification-success-system
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Fortinet|FortiGate-""", """|system""" ]
 } 

${FortinetParsersTemplates.fortinet-fortigate-cef-network-traffic-info}{
   Name = fortinet-fortigate-kv-network-notification-success-vpn
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Fortinet|FortiGate-""", """|vpn""" ]
 

}
```