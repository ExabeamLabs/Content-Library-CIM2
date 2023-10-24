#### Parser Content
```Java
{
Name = cisco-ac-str-vpn-login-success-734001
    ParserVersion = v1.0.0
    Vendor = Cisco
    Product = AnyConnect
    TimeFormat = ["MMM dd yyyy HH:mm:ss","yyyy-MM-dd'T'HH:mm:ssZ"]
    Conditions = [ """Connection AnyConnect: The following DAP records were selected for this connection: DfltAccessPolicy"""] 
    Fields = [
      """\w{1,3}\s{1,2}\d{1,2}\s\d\d:\d\d:\d\d\s({host}[\w.\-]+)\s%ASA-""",
      """({host}[^\s]+)\s+:\s+%FTD-""",
      """User\s(({email_address}[^@,]+@[^,]+)|(({domain}[^\\,]+)\\+)?({user}[\w\.\-]{1,40}\$?))""",      
      """User\s+({full_name}[^,@]+\s\w+)""",
      """Addr\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """({time}\w+ \d+ \d\d\d\d \d+:\d+:\d+)\s*(({host}[\w.\-]+))?.*?%(ASA|FTD)-""",
      """({time}\d{1,4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}Z?)""",
      """%FTD-({priority}\d+)-({event_code}\d+)"""
   ]
  

}
```