#### Parser Content
```Java
{
Name = auth0-a-json-endpoint-login-fail-fp
Conditions = [
  """type":"fp"""
  """user_id"""
  """client_name"""
  """client_id"""
]
ParserVersion = "v1.0.0"

cef-aruba-nac-logon = {
  Vendor = HP
  TimeFormat = "epoch"
  Fields = [
    """\Wrt=({time}\d+)""",
    """\Wdvc=({host}.+?)\s+(w+=|$)""",
    """\Wdvchost=({host}.+?)\s+([\w\.]+=|$)""",
    """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
    """\Wduser=(?:({user_type}host)/)?(({domain}[^\\=]+)\\+)?({user}[^\s\\\/=\.]+)?\s+([\w\.]+=|$)""",
    """\Wdpriv=({access_type}.+?)\s+([\w\.]+=|$)""",
    """\Wdmac=({dest_mac}.+?)\s+([\w\.]+=|$)""",
    """\Wad\.ArubaClearpassRADIUSAcctNASPortType=({network}.+?)\s+([\w\.]+=|$)""",
    """\Wad\.ArubaClearpassRADIUSAcctSessionId=({session_id}.+?)\s+([\w\.]+=|$)""",
    """\Wdst=({dest_ip}.+?)\s+([\w\.]+=|$)""",
    """\Wcs1=({session_id}[^\s]+).*?cs1Label=Session Id""",
    """cs1Label=Session Id.*?\Wcs1=({session_id}[^\s]+)""",
    """\Wcs3=({network}[^\s]+).*?cs3Label=Port Type""",
    """cs3Label=Port Type.*?\Wcs3=({network}[^\s]+)""",

  ]
  DupFields = [ "dest_ip->auth_server" 
}
```