#### Parser Content
```Java
{
Name = unix-unix-cef-app-activity-sendmail
   Vendor = Unix
   Product = Unix 
   ParserVersion = "v1.0.0"
   TimeFormat = "epoch"
   Conditions = [  """CEF""","""Unix|Sendmail"""    ]
   Fields = [
      """\Wrt=({time}\d{13})""",
      """\Wdvc=({host}[^\s]+)""",
      """\Wdvchost=({host}[^\s]+)""",
      """CEF:([^\|]*\|){4}({additional_info}[^\|]+)""",
      """CEF:([^\|]*\|){5}({event_code}[^\|]+)""",
      """\WeventId=({alert_id}\d+)""",
      """\Wduser=({user}[\w\.\-]{1,40}\$?)(@({domain}[^\s]+))?""",
      """\Wduid=({email_address}[^\s]+)""",
   ]
 

}
```