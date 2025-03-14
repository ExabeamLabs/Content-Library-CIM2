#### Parser Content
```Java
{
Name = dg-ndlp-kv-email-send-success-28
  ParserVersion = v1.0.0
  Product = Digital Guardian Network DLP
  Conditions = [ """ Agent_Local_Time="""", """ User_Name ="""", """ Operation="28"""" ]
  Fields = ${DGParsersTemplates.digital-guardian-activity.Fields}[
    """Email_Sender="({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""",
    """Email_Subject="\s*({email_subject}[^"]+?)\s*"""",
    """Email_Recipient="(?i)(unknown|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""""
  ]

digital-guardian-activity = {
  Vendor = Digital Guardian
  Product = Digital Guardian
  TimeFormat = "MM/dd/yyyy HH:mm:ss a"
  Fields = [
    """Agent_Local_Time="({time}\d+\/\d+\/\d\d\d\d\s\d+:\d+:\d+\s(AM|PM|am|pm))""",
    """\w+\s\d\d\s\d\d:\d\d:\d\d\s*({host}[\w\-.]+)\s\w+=""",
    """\sComputer_Name ="(({domain}[^\\]+)?\\?({src_host}[^"]+))""",
    """\sUser_Name ="(({domain}[^\\]+)?\\?({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """\sSource_Directory="({src_file_dir}[^=]+?)\s*"\s*\w+=""",
    """\sDestination_Directory="({file_dir}[^=]+?)\s*"\s*\w+=""",
    """\sDestination_File="({file_name}[^="]+?(\.({file_ext}[^"\s\.]+?))?)\s*"\s*\w+=""",
    """\sOperation="({event_code}\d+)""",
    """\sApplication="({process_name}[^"]+)""",
    """\sSource_File="({src_file_name}[^=]+?)\s*"\s*\w+=""",
  
}
```