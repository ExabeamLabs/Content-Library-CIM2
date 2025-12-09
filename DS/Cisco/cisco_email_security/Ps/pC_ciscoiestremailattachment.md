#### Parser Content
```Java
{
Name = cisco-ie-str-email-attachment
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = Cisco Email Security
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [ """MID """, """ attachment """ ]
    Fields = [
      """MID ({message_id}({alert_id}\d+)) attachment '({attachment}({email_attachment}[^']+))'""",
      """attachment '({email_attachment}[^']+\.({file_ext}[^']+))'""",
       ]
  

}
```