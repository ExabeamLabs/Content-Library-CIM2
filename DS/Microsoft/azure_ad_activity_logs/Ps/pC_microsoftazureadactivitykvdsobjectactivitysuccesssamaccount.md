#### Parser Content
```Java
{
Name = microsoft-azureadactivity-kv-ds-object-activity-success-samaccount
    ExtractionType = regex
    Vendor = Microsoft
    Product = Azure AD Activity Logs
    ParserVersion = v1.0.0
    TimeFormat = [ "MM/dd/yyyy HH:mm:ss.SSS", "MM/dd/yyyy HH:mm:ss" ]
    Conditions = [ "whenChanged=", "distinguishedName =", "sAMAccountType=", "sAMAccountName =", "accountExpires=", "pwdLastSet=", "Event Details" ]
    Fields = [ 
      """({time}\d+\/\d+\/\d+ \d+:\d+:\d+\.\d+)""", 
      """(?i)distinguishedName =({object_dn}\S+)\s""", 
      """(?i)\swhenChanged=({operation_last}[^=]+?)\s*\w+=""", 
      """(?i)\sdescription=({description}[^=]+?)\s*\w+=""", 
      """(?i)\sgivenName =({first_name}\w+)\s""", 
      """(?i)\ssn=({last_name}\w+)\s""", 
      """(?i)\sobjectCategory=({object_type}[^\}]+?)\s+name=({account_name}[\w\-]+)\s""", 
      """(?i)\sobjectCategory=({object_type}[^\}]+?)\s+name=({server_name}[\w\-]+)\s""", 
      """(?i)operatingSystemVersion=({os_version}[^=]+?)\s+operatingSystem=({os}[^=]+?)\s+\w+=""" ,
      """userPrincipalName =(({email_address}[^\s=@]+@[^@\s=]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """\shost="({host}[^"]+)""""
	]


}
```