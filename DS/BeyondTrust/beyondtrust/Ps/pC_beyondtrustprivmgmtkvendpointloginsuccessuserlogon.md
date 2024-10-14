#### Parser Content
```Java
{
Name = beyondtrust-privmgmt-kv-endpoint-login-success-userlogon
    Vendor = BeyondTrust
    Product = BeyondTrust
    TimeFormat = "MM/dd/yyyy HH:mm:ss a"
    Conditions = [ """SourceName =Avecto Defendpoint Service""", """Message=Detected user logon"""]
    Fields = [
      """ComputerName =({host}[^\s]+)""",
      """Message=({operation_type}.+?)\s+Command Line:""",
      """User Name:\s*(?:[A-F\d\-]{36}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+User Domain SID:""",
      """User Domain Name:\s*({domain}[\w\.\-]{1,40}?)\s+User Domain Name""",
      """User SID:\s*({user_sid}.*?)\s+User Name""",
      """Administrator:\s*({admin}.*?)\s+Power User""",
      """Power User:\s*({power_user}.*?)\s+Workstyle""",
      """Workstyle:\s*({user_info}.*?)\s+Workstyle""",
      """IP4 Addresses:\s*[^,]+,({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(,|$|\s)""",
    ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = v1.0.0


}
```