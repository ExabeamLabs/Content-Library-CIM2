#### Parser Content
```Java
{
Name = cisco-asa-kv-vpn-logout-success-rsasalog
    Vendor = Cisco
    Product = Cisco Adaptive Security Appliance
    TimeFormat = "MMM dd yyyy HH:mm:ss"
    Conditions = [ """Authen Session End:""", """rsa_sa_log""" ]
    Fields = [ 
      	       """({time}\w+ \d+ \d\d\d\d \d\d:\d\d:\d\d):""",
               """Authen Session End: user '({user}[\w\.\-]{1,40}\$?)'""" 
	]
	ParserVersion = "v1.0.0"
  

}
```