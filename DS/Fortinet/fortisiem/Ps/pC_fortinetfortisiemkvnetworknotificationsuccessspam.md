#### Parser Content
```Java
{
Name = "fortinet-fortisiem-kv-network-notification-success-spam"
  ParserVersion = "v1.0.0"
  Conditions = [ """devname="FortiMail"""", """type="spam"""", """subtype="""", """msg="""" ]
  Fields = ${FortinetParsersTemplates.fortisiem-fortimail-email-traffic-activity.Fields}[
    """\Waction="({operation}[^"]+)"""",
    """\Wstatus="({result}[^"]+)"""",
    """\Wreason="({failure_reason}[^"]+)"""",
  ]

fortisiem-fortimail-email-traffic-activity = {
  Vendor = Fortinet
  Product = FortiSIEM
  TimeFormat = "epoch_sec"
  Fields = [
    """\Wtimestamp=({time}\d{10})""",
    """\Wdevname="({dest_host}({host}[\w\-.]+))""",
    """\Wdevice_id="({device_id}[^"]+)""",
    """\Wtype=({category}[^"]+)""",
    """\Wsubtype="({event_category}[^"]+)"""",
    """\Wpri="({severity}[^"]+)"""",
    """\Wmsg="({event_name}[^"]+)""",
    """\Wsession_id="({session_id}[^"]+)""",
    """\Wclient_name="({src_host}[^"]+)""",
    """\Wclient_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\Wdst_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """\Wfrom="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\Wto="({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
  
}
```