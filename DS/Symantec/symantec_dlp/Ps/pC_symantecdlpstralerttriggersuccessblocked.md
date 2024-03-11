#### Parser Content
```Java
{
Name = symantec-dlp-str-alert-trigger-success-blocked
	ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec DLP
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """ PROTOCOL """, """ POLICY """, """ MATCHES """, """ SEVERITY """, """ BLOCKED """, """ URL """, """ SENDER """, """ RECIPIENTS """, """ FILE_NAME """, """ PARENT_PATH """ ]
    Fields = [
    """\sFILE_NAME\s(?:N\/A|({email_attachments}({file_name}.+?)))\sPARENT_PATH\s""",
    """\sSENDER\s\w+:\/\/({domain}[^\<\>\[\]\"\/\\:;\|=,+*\?]+)\/({user}[^\<\>\[\]\"\/\\:;\|=,+*\?]+?)\sRECIPIENTS\s""",
    """\sSENDER\s({src_email_address}[^\s"@,]+@({domain}[^\s"@,]+))\sRECIPIENTS\s""",
    """\sSENDER\s({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\sRECIPIENTS\s""",
    """\sBLOCKED\s(?:N\/A|({action}.+?))\sURL\s""",
    """\sSEVERITY\s(?:N\/A|({alert_severity}.*?))\sBLOCKED\s""",
    """\sINCIDENT\s(?:N\/A|({alert_id}\d{1,100}?))\sPOLICY\s""",
    """\sPOLICY\s(?:N\/A|({alert_type}.+?))\sMATCHES\s""",
    """\sPROTOCOL\s(?:N\/A|({protocol}.+?))\sINCIDENT\s""",
    """\sRECIPIENTS\s({target}(http:\/\/|https:\/\/).+?)\/.*?\sFILE_NAME\s""",
    """\sRECIPIENTS\s(?:N\/A|https:\/\/.+?|http:\/\/.+?|Unknown|({dest_email_address}[^,]+?))[\s\,]""",
    """\sRECIPIENTS\s(?:N\/A|https:\/\/.+?|http:\/\/.+?|Unknown|({email_recipients}.+?))\s""",
    ]
    DupFields = [ "alert_type->alert_name" , "dest_email_address->external_address" ]
  

}
```