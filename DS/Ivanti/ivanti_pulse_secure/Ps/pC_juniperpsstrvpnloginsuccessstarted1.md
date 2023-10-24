#### Parser Content
```Java
{
Name = juniper-ps-str-vpn-login-success-started-1
    ParserVersion = v1.0.0
    Vendor = Ivanti
    Product = Ivanti Pulse Secure
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Conditions = ["""VPN Tunneling:""",
""": Session started for user"""
]
    Fields = [
	    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d[+-]\d\d:\d\d)\s({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}|[\w\-\.]{1,2000})\s*(Juniper|PulseSecure):""",
	    """with IP(?:v4 address)?\s+({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
	    """\- \[({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\]\s+([\w\s]+?::)?(({domain}[^\\]+)\\)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))\(({realm}[^\[]+)?\)\[(?!Machine Cert)""",
	    """,\s{1,100}hostname\s+({src_host}[\w.\-]+)""",
	    """({event_name}Session started)""",
    ]
    DupFields = [ "host->dest_host" , "user->account" ]
  

}
```