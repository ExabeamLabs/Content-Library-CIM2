#### Parser Content
```Java
{
Name = microsoft-o365-cef-app-activity-success-addmailboxpermission
  Vendor = Microsoft
  Product = Microsoft 365
  ParserVersion = v1.0.0
  ExtractionType = json
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ssZ"]
  Conditions = [ """"ResultStatus"""" , """Add-MailboxPermission""", """"Workload":""", """"Operation":"""" ]
  Fields = [
    """exa_json_path=$..CreationTime,exa_field_name=time"""
    """exa_json_path=$..Operation,exa_field_name=operation"""
    """exa_json_path=$..ObjectId,exa_field_name=object_id"""
    """exa_json_path=$..ResultStatus,exa_field_name=result"""
    """exa_json_path=$..OriginatingServer,exa_regex=({host}\w+)"""
    """exa_json_path=$.UserId,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """exa_json_path=$..UserKey,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)"""
    """exa_json_path=$..DeviceId,exa_field_name=device_id"""
    """exa_json_path=$..AppAccessContext,exa_field_name=additional_info"""
    """exa_json_path=$..AppPoolName,exa_field_name=app"""
    """exa_json_path=$..Workload,exa_field_name=app"""
    """exa_json_path=$..UserType,exa_field_name=user_type"""
    """exa_json_path=$..ClientAppId,exa_field_name=app_id"""
    """exa_json_path=$..AppId,exa_field_name=app_id"""
    """exa_json_path=$..SessionId,exa_field_name=session_id"""
    """exa_json_path=$..ClientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """exa_json_path=$..OrganizationName,exa_field_name=company"""
    """exa_json_path=$..Parameters[?(@.Name == 'AccessRights')].Value,exa_field_name=access"""
    """exa_json_path=$..Parameters[?(@.Name == 'Identity')].Value,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))"""
    """exa_json_path=$..Parameters[?(@.Name == 'User')].Value,exa_regex=(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
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
     """"(?i)UserId":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)""""
   ]


}
```