#### Parser Content
```Java
{
Name = mcafee-dlp-cef-email-send-success-protectedcontent
    Vendor = McAfee
    Product = McAfee DLP
    TimeFormat = "epoch"
    Conditions = [ """|McAfee|DLP Prevent|""", """The content was categorized as protected content""" ]
    Fields = [
      """\w{3} \d{1,2} \d{1,2}:\d{1,2}:\d{1,2}\s*({host}[\w\-\.]+)\s*""",
      """(\s|\|)rt=({time}\d{13})""",
      """CEF:([^|]+?\|){5}({alert_type}[^|]+)""",
      """CEF:([^|]+?\|){6}({alert_severity}[^|]+)""",
      """(\s|\|)app=({protocol}.+?)\s+\w+=""",
      """(\s|\|)msg=({alert_name}.+?)\s*(\w+=|$)""",
      """(\s|\|)dst=({dest_ip}(\d{1,3}\.){3}\d{1,3})""",
      """(\s|\|)dhost=({dest_host}[^\s]+)""",
      """(\s|\|)src=({src_ip}(\d{1,3}\.){3}\d{1,3})""",
      """(\s|\|)shost=({src_host}[^\s]+)""",
      """(\s|\|)suser=(?:<>|<?({sender}[^\s>]+)>?)\s*(\w+=|$)""",
      """(\s|\|)duser=({email_recipients}.*?)\s*(\w+=|$)""",
      """(\s|\|)duser=<({external_address}[^@<]+@?[^\s,>]+)>""",
      """(\s|\|)fsize=({bytes}\d+)""",
      """\scs4=({email_attachment}.+?)\s*(\w+=|$)""",
      """\scs6=({email_subject}.+?)\s*(\w+=|$)""",
      """\scn3=({num_recipients}\d+)""",
      """\scn2=({num_attachments}\d+)""",
      """\sfilePath=(({file_path}[^\s]+\\)?({file_name}[^\s]+\.({file_ext}[^\s]+)))""",
    ]
    DupFields = [ "sender->user" ]
	ParserVersion = "v1.0.0"
  

}
```