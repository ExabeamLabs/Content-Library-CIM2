#### Parser Content
```Java
{
Name = fortinet-fortigate-kv-network-notification-success-connectorevent
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Fortinet|FortiGate-""", """|connector event|""" ]
 } 

${FortinetParsersTemplates.fortinet-fortigate-cef-network-traffic-info}{
   Name = fortinet-fortigate-kv-network-notification-success-fortiextender
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Fortinet|FortiGate-""", """|fortiextender""" ]
 

}
```