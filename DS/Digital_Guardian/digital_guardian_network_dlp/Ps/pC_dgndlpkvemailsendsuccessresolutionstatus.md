#### Parser Content
```Java
{
Name = dg-ndlp-kv-email-send-success-resolutionstatus
  ParserVersion = v1.0.0
  Product = Digital Guardian Network DLP
  Conditions = [ """ Policy=""" , """ Resolution_Status=""" ]

splunk-digitalguardian-dlp-alert = {
  Vendor = Digital Guardian
  Product = Digital Guardian Network DLP
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Fields = [
    """[^_](Agent_UTC_Time|Server_UTC_Timestamp)="({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (am|AM|pm|PM))"""",
    """[^_]Computer_Name ="([^\/\\"]+[\/\\]+)?({host}[^"]+)"""",
    """[^_]User_Name ="(?:|(({domain}[^"\/\\]+)[\/\\]+)?({user}[\w\.\-]{1,40}\$?))"""",
    """[^_]Domain_Name ="(?:|({domain}[^"]+))"""",
    """[^_]Rule="({alert_name}[^"]+)""",
    """[^_]Operation="({alert_type}[^"]+)""",
    """[^_]Protocol="({protocol}[^"]+)""",
    """[^_]Severity="({alert_severity}[^"]+)"""",
    """[^_]Destination_Device_ID="({device_id}[^"]+)"""",
    """[^_]Source_File="(?:|({file_name}[^"]+))"""",
    """[^_]Destination_File="(?:|({file_name}[^"]+))"""",
    """[^_]Bytes_Written="(?:|({bytes}\d+))"""",
    """[^_]IP_Address="(?:|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)"""",
    """[^_]Application="(?:|({process_name}[^"]+))"""",
    """[^_]Email_Recipient="(?:|({target}[^"]+))"""",
    """[^_]Computer_Type="(?:|({os}[^"]+))""""
  ]
  DupFields = [ "host->src_host" ]
  SOAR {
    IncidentType = "dlp"
    DupFields = ["time->startedDate", "vendor->source", "rawLog->sourceInfo", "user->dlpUser", "alert_name->dlpPolicy", "protocol->dlpProtocol", "src_host->dlpDeviceName", "file_name->dlpFileName", "bytes->dlpFileSize"]
    NameTemplate = """Digital Guardian DLP Alert ${alert_name} found"""
    ProjectName = "SOC"
    EntityFields = [
      {EntityType="device", Name ="src_address", Fields=["src_host->host_name"]},
      {EntityType="device", Name ="dest_address", Fields=["dest_ip->ip_address"]},
      {EntityType="user", Name ="windows_id", Fields=["user->windows_id"]}
    ]
    }
  },

  leef-digitalguardian-dlp-email-alert-out = {
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w\-.]+) LEEF:""",
    """accountName =(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s*(\w+=|$)""",
    """IdentHostName =(({domain}[^\\])+\\+)?({dest_host}[\w\-.]+?)\s*(\w+=|$)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """EmailSender=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s*(\w+=|$)""",
    """usrName =(?![^\s]+@[^\s]+)(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s*(\w+=|$)""",
    """usrName =(?=[^\s]+@[^\s]+)({email_address}[^\s@]+@[^\s]+)""",
    """EmailRecipient=(|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""",
    """EmailRecipient=(|({email_recipients}.+?))\s*(\w+=|$)""",
    """EmailRecipient=({external_address}[^@]+@[^@\s,;]+).*?\s*(\w+=|$)""",
    """EmailSubject=(|({email_subject}.+?))\s*(\w+=|$)""",
    """sev=({alert_severity}\d+)""",
    """srcBytes=({bytes}\d+)""",
    """FileSizeMB=({bytes}\d+)""",
    """FileSize({bytes_unit}MB)""",
    """DestinationFile=(|({email_attachments}[^\.]+\.({file_ext}.+?)))\s*(\w+=|$)""",
  
}
```