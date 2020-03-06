# WAYFless

&emsp;&emsp;WAYFless 是一种通过将IDP地址组合在 URL中，避免读者在采用[Shibboleth](http://www.shibboleth.net/)认证时必须先选择自己所在机构的方法，省去了不同 SP界面 各不相同的复杂认证步骤。

&emsp;&emsp;目前支持Shibboleth的数据库中提供WAYFless-URL的(使用时，请把URL中的“{IDP地址}”替换为本校的IDP地址，比如idp.xxx.edu.cn)如下所示。

&emsp;&emsp;加入[CARSI](https://www.carsi.edu.cn/)联盟的各个学校均可使用此方式，方便读者使用。

&emsp;&emsp;本词条由深圳大学图书馆、香港中文大学(深圳)图书馆、清华大学图书馆共同维护。

# WAYFless Shibboleth URL List
## EBSCO
### 方式1
    https://shibboleth.ebscohost.com/Shibboleth.sso/Login?SAMLDS=1&target=https%3A%2F%2Fshibboleth.ebscohost.com%2FShibAgent.aspx%3Fshib_returl%3Dhttps%253a%252f%252fsearch.ebscohost.com%252flogin.aspx%253fauthtype%253dshib%26IdpId%3D&entityID=https://{IDP地址}/idp/shibboleth&providerID=http://shibboleth.ebscohost.com

### 方式2(官方提供)
    http://search.ebscohost.com/login.aspx?authtype=ip,shib&custid={customer ID} 
    Customer ID 需要向EBSCO获取
## Emerald Management
    https://www.emerald.com/start-session?idp=https://{IDP地址}/idp/shibboleth
## Engineering Village
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=https%3A%2F%2Fwww.engineeringvillage.com%2Fsearch%2Fquick.url
## ProQuest
### 方式1
    https://shibboleth-sp.prod.proquest.com/Shibboleth.sso/DS?SAMLDS=1&target=https%3A%2F%2Fshibboleth-sp.prod.proquest.com%2FONE_SEARCH%2FPROD&entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth
### 方式2(官方提供)
    https://search.proquest.com/?accountid={account ID}
    account ID 需要向ProQuest获取
## IEEE/IET ELECTRONIC LIBRARY（IEL）
    https://ieeexplore.ieee.org/servlet/wayf.jsp?entityId=https://{IDP地址}/idp/shibboleth&url=https%3A%2F%2Fieeexplore.ieee.org
## IOP Journals
    https://myiopscience.iop.org/signin?origin=deeplink&entity=https://{IDP地址}/idp/shibboleth&target=https://iopscience.iop.org/
## Nature
    https://sp.nature.com/saml/login?idp=https://{IDP地址}/idp/shibboleth&targetUrl=https://www.nature.com/nature
## Reaxys
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=https%3A%2F%2Fwww.reaxys.com%2F%23%2Fsearch%2Fquick
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
    https://www.webofknowledge.com/?auth=ShibbolethIdPForm&entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&target=https%253A%252F%252Fwww.webofknowledge.com%252F%253FDestApp%253DUA&ShibFederation=ChineseFederation&DestApp=UA
## CNKI
    https://fsso.cnki.net/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https://fsso.cnki.net/secure/default.aspx
## JoVE
    https://www.jove.com/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fwww.jove.com%2Fshibboleth%2Fwayf_login.php%3Freturn_page=http://www.jove.com/
## Embase
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=http%3A%2F%2Fwww.embase.com%2Fcustomer%2Fauthenticate%3Fauth_type%3DSHIBBOLETH
## OVID
    https://openathens.ovid.com/secure-ssl/home.oa?idpselect=https://{IDP地址}/idp/shibboleth&entityID=https://{IDP地址}/idp/shibboleth&T=JS&CSC=y&PAGE=dblist&NEW
## Wiley
    https://onlinelibrary.wiley.com/action/ssostart?idp=https://{IDP地址}/idp/shibboleth&redirectUri=https://onlinelibrary.wiley.com/
## Cambridge
注意，两种方式有时候认证通过后仍然会出现选择机构的界面，目前数据库商反馈说短时间内无法解决。
### 方式1（官方提供）
    https://www.cambridge.org/core/idp/{customer ID}
    customer ID 需要向 Cambridge 获取
### 方式2
    https://shibboleth.cambridge.org/Shibboleth.sso/discovery?entityID=https://{IDP地址}/idp/shibboleth&target=https://shibboleth.cambridge.org/CJOShibb2/index?app=https://www.cambridge.org/core/shibboleth
## Oxford Journals Collection
    https://shibboleth2sp.sams2.oup.com/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https://shibboleth2sp.sams2.oup.com/shib?dest=https%3A%2F%2Facademic.oup.com%2FSHIBBOLETH%3Fdest%3D%252Fjournals%252F
## ClinicalKey
    https://auth.elsevier.com/ShibAuth/institutionLogin?appReturnURL=https%3A%2F%2Fwww.clinicalkey.com%2Fshibboleth%2F&entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth
## Heinonline
    https://heinonline.org/HOL/oa/login?entityID=https://{IDP地址}/idp/shibboleth
## 万方
    https://shibboleth.wanfangdata.com.cn/Shibboleth.sso/Login?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&target=https%3A%2F%2Fshibboleth.wanfangdata.com.cn%2F
## Jstor
    https://shibbolethsp.jstor.org/start?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&site=jstor&dest=%2F
