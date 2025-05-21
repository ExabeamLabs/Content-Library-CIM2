#### Parser Content
```Java
{
Name = checkpoint-ngfw-kv-email-receive-mtainbound
  Vendor = "Check Point"
  Product = "Check Point NGFW"
  TimeFormat = "epoch_sec"
  Conditions = [ """ CheckPoint """, """product:"MTA"""", """ifdir:"""", """email_status:"""" ]
  Fields = [
    """\Wtime:"({time}\d{10})"""",
    """\W({host}[\w\-.]+) CheckPoint""",
    """\Wdst:"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
    """\Wsrc:"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\Worigin:"({origin_ip}[^"]+)""",
    """\Wfrom:"({email_address}((?=.{1,64}\@)([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+)@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""",
    """\Wto:"({email_recipients}({dest_email_address}((?=.{1,64}\@)([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+)@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))""""
    """\Wemail_subject:"\s*({email_subject}[^"]+?)\s*""""
    """\Wemail_status:"({action}[^"]+)"""
    """\W\Wfailure_reason:"({failure_reason}[^"]+)"""
    """\Wemail_message_id:"({message_id}[^"]+)"""
    """\Wemail_content:"({additional_info}[^"]+)"""
    """file_size:"({bytes}\d+)""""
  ]
  ParserVersion = "v1.0.0"


}
```