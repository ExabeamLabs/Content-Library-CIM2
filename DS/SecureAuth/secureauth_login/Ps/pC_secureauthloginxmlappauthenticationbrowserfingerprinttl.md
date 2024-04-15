#### Parser Content
```Java
{
Name = "secureauth-login-xml-app-authentication-browserfingerprint-tl"
    ParserVersion = "v1.0.0"
    Vendor = "SecureAuth"
    Product = "SecureAuth Login"
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Conditions = [
      "<userid>"
      ": state [init_logon]"
      "<category>debug</category>"
      "allowedtokens = browserfingerprint"
    ]
    Fields = [
      "(?i)Host\\s=\\s({host}[^;]+)"
      "(?i)<Category>({category}[^<]+)"
      "(?i)User-Agent\\s=\\s({user_agent}.+?);\\s*CompanyID\\s="
      "(?i)CompanyID\\s=\\s({company}.+)\\sCookieName\\s="
    ]
  

}
```