#### Parser Content
```Java
{
Name = microsoft-o365-cef-app-activity-success-addmailboxpermission
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """"ResultStatus"""" , """Add-MailboxPermission""", """"Workload":""", """"Operation":"""" ]
  Fields = [
     """"CreationTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
     """flexString1=({operation}[^=]*?)\s\w+=""",
     """\sby\s\[({email_address}[^@]+@({email_domain}[^\]]*))\]""",
     """ObjectId":"({resource}[^"]*)"""",
     """ResultStatus":"({result}[^"]*)"""",
     """Name":"AccessRights","Value":"({additional_info}[^"]*)"""",
     """destinationServiceName =({app}[^\<"=,:]+)\s+""",
     """ClientIP":"\[?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\]?(:\d{5})""",
     """duser=([^=]+\/)?({object}.+?)(\s+\w+=|\s*$)""",
     """"OriginatingServer":"({host}[\w\-.]+)\s""",
     """"Operation":"({operation}[^"]+)"""",
     """\sduser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\s""",
     """"Name":"Identity"[^\}]+?"Value":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
     """\ssuser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)\s""",
     """"UserId":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""""
   ]


}
```