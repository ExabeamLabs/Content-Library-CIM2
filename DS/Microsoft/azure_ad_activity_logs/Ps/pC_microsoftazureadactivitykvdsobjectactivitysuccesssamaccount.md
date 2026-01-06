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
      """distinguishedName =({object_dn}\S+)\s""", 
      """\swhenChanged=({operation_last}[^=]+?)\s*\w+=""", 
      """\sdescription=({description}[^=]+?)\s*\w+=""", 
      """\sgivenName =({first_name}\w+)\s""", 
      """\ssn=({last_name}\w+)\s""", 
      """\sobjectCategory=({object_type}[^\}]+?)\s+name=({account_name}[\w\-]+)\s""", 
      """\sobjectCategory=({object_type}[^\}]+?)\s+name=({server_name}[\w\-]+)\s""", 
      """operatingSystemVersion=({os_version}[^=]+?)\s+operatingSystem=({os}[^=]+?)\s+\w+=""" ,
      """userPrincipalName =(({email_address}[^\s=@]+@[^@\s=]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
      """\shost="({host}[^"]+)""""
	]


}
```