#### Parser Content
```Java
{
Name = ironscales-is-cef-app-notification-success-report
 Conditions = ["""CEF:""", """|IronScales|IronTraps|""", """report""" ]
 ParserVersion = v1.0.0

ironscales-cef-template = {
      Vendor = "Ironscales"
      Product = "Ironscales"
      TimeFormat = "MMM dd HH:mm:ss"
      Fields = [
        """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s+\S+\s+CEF:""",
        """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
        """duser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
        """cs5=({result}[^=]+?)\s+cs5Label=Report State"""
        """reason=({additional_info}[^=]+?)\s+\w+="""
        """request=({malware_url}[^\s]+)"""
        """cs4=({email_subject}[^=]+?)\s+cs4Label=(?i)(Email Subject)"""
        """CEF:([^\|]+\|){5}(\d+|({event_name}[^\|]+))\|"""
        """cs6=({result}\S+)\s+cs6Label=(?i)Outcome"""
        """cs2=({full_name}[^=]+)\s+cs2Label=Employee Name"""
      ]
    
}
```