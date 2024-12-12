#### Parser Content
```Java
{
Name = fortinet-fortigate-kv-network-notification-success-vpn
   ParserVersion = v1.0.0
   Conditions = [ """CEF:""", """|Fortinet|FortiGate-""", """|vpn""" ]
 }  

${FortinetParsersTemplates.fortisiem-fortimail-email-traffic-activity}{
  Name = "fortinet-fortisiem-kv-network-notification-success-spam"
  ParserVersion = "v1.0.0"
  Conditions = [ """devname="FortiMail"""", """type="spam"""", """subtype="""", """msg="""" ]
  Fields = ${FortinetParsersTemplates.fortisiem-fortimail-email-traffic-activity.Fields}[
    """\Waction="({operation}[^"]+)"""",
    """\Wstatus="({result}[^"]+)"""",
    """\Wreason="({failure_reason}[^"]+)"""",
  ]


}
```