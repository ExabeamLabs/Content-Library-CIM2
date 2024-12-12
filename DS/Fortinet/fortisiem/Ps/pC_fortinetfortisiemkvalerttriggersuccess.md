#### Parser Content
```Java
{
Name = "fortinet-fortisiem-kv-alert-trigger-success"
  ParserVersion = "v1.0.0"
  Conditions = [ """devname="FortiMail"""", """type="virus"""", """subtype="infected"""" ]
  Fields = ${FortinetParsersTemplates.fortisiem-fortimail-email-traffic-activity.Fields}[
    """\Wsignature_id="({additional_info}[^"]+)"""",
    """\Wvirus_name="({malware_file_name}[^"]+)""""  
  ]
  DupFields = ${FortinetParsersTemplates.fortisiem-fortimail-email-traffic-activity.DupFields}[ "severity->alert_severity", "event_name->alert_name", "category->alert_type", "event_category->alert_subject" ]  

fortisiem-fortimail-email-traffic-activity = {
  Vendor = Fortinet
  Product = FortiSIEM
  TimeFormat = "epoch_sec"
  Fields = [
    """\Wtimestamp=({time}\d{10})""",
    """\Wdevname="({host}[\w\-.]+)""",
    """\Wdevice_id="({device_id}[^"]+)""",
    """\Wtype=({category}[^"]+)""",
    """\Wsubtype="({event_category}[^"]+)"""",
    """\Wpri="({severity}[^"]+)"""",
    """\Wmsg="({event_name}[^"]+)""",
    """\Wsession_id="({session_id}[^"]+)""",
    """\Wclient_name="({src_host}[^"]+)""",
    """\Wclient_ip="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
    """\Wdst_ip="({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """\Wfrom="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
    """\Wto="({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
  ]
  DupFields = [ "host->dest_host" 
}
```