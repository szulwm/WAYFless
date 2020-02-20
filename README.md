# WAYFless

&emsp;&emsp;WAYFless 是一种通过将IDP地址组合在 URL中，避免读者在采用[Shibboleth](http://www.shibboleth.net/)认证时必须先选择自己所在机构的方法，省去了不同 SP界面 各不相同的复杂认证步骤。

&emsp;&emsp;目前支持Shibboleth的数据库中提供WAYFless Shibboleth URL的(使用时，请把URL中的“{IDP地址}”替换为本校的IDP地址，比如idp.xxx.edu.cn)如下所示。

&emsp;&emsp;加入[CARSI](https://www.carsi.edu.cn/)联盟的各个学校均可使用此方式，方便读者使用。

&emsp;&emsp;本词条由深圳大学图书馆、香港中文大学(深圳)图书馆、清华大学图书馆共同维护。

# WAYFless Shibboleth URL List
## EBSCO
    https://shibboleth.ebscohost.com/Shibboleth.sso/Login?SAMLDS=1&target=https%3A%2F%2Fshibboleth.ebscohost.com%2FShibAgent.aspx%3Fshib_returl%3Dhttps%253a%252f%252fsearch.ebscohost.com%252flogin.aspx%253fauthtype%253dshib%26IdpId%3D&entityID=https://{IDP地址}/idp/shibboleth&providerID=http://shibboleth.ebscohost.com
## Emerald Management
    https://www.emerald.com/start-session?idp=https://{IDP地址}/idp/shibboleth
## Engineering Village
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=https%3A%2F%2Fwww.engineeringvillage.com%2Fcustomer%2Fauthenticate.url%3Fauth_type%3DSHIBBOLETH
## ProQuest
    https://shibboleth-sp.prod.proquest.com/Shibboleth.sso/DS?SAMLDS=1&target=https%3A%2F%2Fshibboleth-sp.prod.proquest.com%2FONE_SEARCH%2FPROD&entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth
## IEEE/IET ELECTRONIC LIBRARY（IEL）
    https://ieeexplore.ieee.org/servlet/wayf.jsp?entityId=https://{IDP地址}/idp/shibboleth&url=https%3A%2F%2Fieeexplore.ieee.org
## IOP Journals
    https://myiopscience.iop.org/signin?origin=deeplink&entity=https://{IDP地址}/idp/shibboleth&target=https://iopscience.iop.org/
## Nature
    https://sp.nature.com/saml/login?idp=https://{IDP地址}/idp/shibboleth&targetUrl=https://www.nature.com/nature
## Reaxys
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https://{IDP地址}/idp/shibboleth&appReturnURL=https%3A%2F%2Fwww.reaxys.com%2Fservices%2Foauth%2Fshibboleth-sso
## Royal Society of Chemistry
    https://www.rsc.org/rsc-id/account/checkfederatedaccess?instituteurl=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&returnurl=https%3A%2F%2Fpubs.rsc.org
## ScienceDirect
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=https%3A%2F%2Fwww.sciencedirect.com%2Fuser%2Frouter%2Fshib%3FtargetURL%3Dhttps%253A%252F%252Fwww.sciencedirect.com%252F
## Scival
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=http%3A%2F%2Fwww.scival.com%2F
## Scopus
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=https%3A%2F%2Fwww.scopus.com%2F
## Springer Link
    https://fsso.springer.com/federation/init?entityId=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&returnUrl=https%3A%2F%2Flink.springer.com%2F
## SpringerMaterials
    https://fsso.springer.com/federation/init?entityId=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&returnUrl=https%3A%2F%2Fmaterials.springer.com%2F
## Web of Science
    https://www.webofknowledge.com/?auth=ShibbolethIdPForm&target=http%253A%252F%252Fwww.webofknowledge.com%252F%253FIsProductCode%253DYes%2526Error%253DIPError%2526PathInfo%253D%25252F%2526RouterURL%253Dhttp%25253A%25252F%25252Fwww.webofknowledge.com%25252F%2526Domain%253D.webofknowledge.com%2526Src%253DIP%2526Alias%253DWOK5%2526ShibFederation%253DChineseFederation&entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth
## CNKI
    https://fsso.cnki.net/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https://fsso.cnki.net/secure/default.aspx
## JoVE
    https://www.jove.com/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fwww.jove.com%2Fshibboleth%2Fwayf_login.php%3Freturn_page=http://www.jove.com/
## Embase
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=http%3A%2F%2Fwww.embase.com%2Fcustomer%2Fauthenticate%3Fauth_type%3DSHIBBOLETH
