#### Parser Content
```Java
{
Name = "microsoft-azuread-cef-app-signinactivity"
Vendor = "Microsoft"
Product = "Azure AD Sign-In Logs"
TimeFormat = "epoch"
Conditions = [
"""CEF:"""
"""|Microsoft|Azure|"""
"""|Sign-in activity|"""
"""ad.azureconditionalAccessStatus="""
]
Fields = [
"""\Wrt=({time}\d{13})"""
"""\Wdvc=({host}[\w\-.]+)"""
"""\Wapp=({app}[^\"\=]+?)\s+(\w+=|$)"""
"""\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\Wshost=({src_host}[\w\-.]+)"""
"""\Woutcome=({result_code}[^\"\=]+?)\s+(\w+=|$)"""
"""\Wduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
"""\Wduser=({full_name}[^\"\=\s]+?\s+[^\"\=\s]+?)\s+(\w+=|$)"""
"""\Wcs6=({email_address}[^\"\=\s@]+@({email_domain}[^\"\=\s@]+?))\s+(\w+=|$)"""
"""\Wreason=(Other|({failure_reason}[^\"\=]+?))\s+(\w+=|$)"""
"""\Wcs4=({location_country}[^\"\=]+?)\s+(\w+=|$)"""
"""\Wcs3=.*?\"city\":\"({location_city}[^\"]+)"""
"""\Wcs3=.*?\"state\":\"({location_state}[^\"]+)"""
"""\Wcs3=.*?\"geocoordinates\":\{({additional_info}[^\}]+)"""
"""\Wad\.azureconditionalAccessStatus=({result}[^\"\=\.]+?)\s+([\w\.]+=|$)"""
"""CEF:([^\|]*\|){4}({operation}[^\|]+)"""
]
ParserVersion = "v1.0.0"


}
```