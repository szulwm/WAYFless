# WAYFless

&emsp;&emsp;WAYFless 是一种通过将IDP地址组合在 URL中，避免读者在采用[Shibboleth](http://www.shibboleth.net/)认证时必须先选择自己所在机构的方法，省去了不同 SP界面 各不相同的复杂认证步骤。

&emsp;&emsp;目前支持Shibboleth的数据库中提供WAYFless-URL的(使用时，请把URL中的“{IDP地址}”替换为本校的IDP地址，比如idp.xxx.edu.cn)[如下所示](#wayfless-shibboleth-url-list)。

&emsp;&emsp;加入[CARSI](https://www.carsi.edu.cn/)联盟的各个学校均可使用此方式，方便读者使用。

&emsp;&emsp;本词条由深圳大学图书馆、香港中文大学(深圳)图书馆、清华大学图书馆共同维护。

# WAYFless 简介
参考UKFederation的文献[WAYFlessGuidance.pdf](https://www.ukfederation.org.uk/library/uploads/Documents/WAYFlessGuidance.pdf), WAYFLess 分为两种， SP-side WAYFless URL 和  IdP-side WAYFless URL。

## SP-side WAYFless URL
由service proivder（电子数据商）提供，指向SP的网页。分为标准格式和非标准格式，标准格式的SP-side WAFYless URL如下
### SP-side WAYFless URL format
    https://SPHOSTNAME/SESSION_INITIATOR_LOCATION?
    entityID=YOUR_IdP&
    target=RESOURCE_LOCATION
### SP-side WAYFless URL example with a target specified
    https://sp.example.com/start-session?entityID=https://idp.example.com/idp/shibboleth&target=https://sp.example.com/some/webpage.html
非标准的SP-side WAFYless URL需要向数据商获取，比如：
###  SP-side WAYFless URL example
    http://search.ebscohost.com/login.aspx?authtype=ip,shib&custid={customer ID} 

## IdP-side WAYFless URL
指向Idp提供者，即各大高校和机构。可以通过构造相关参数来解决SP端不提供WAYFless URL的电子资源。格式如下：
### IdP-side WAYFless format
    https://IDPHOSTNAME/{SSO_LOCATION}?target=RESOURCE_LOCATION&
    shire={ACS_LOCATION}&
    providerId={PROV_ID}
ACS_LOACTION参数可从shibboleth metadata或者电子数据商处获取。
### IdP-side WAYFless URL example with a target specified
    https://{IDP地址}/idp/profile/Shibboleth/SSO?target=https%3A%2F%2Fdl.acm.org%2F&shire=https%3A%2F%2Fdl.acm.org%2Faction%2FsamlACS&providerId=https%3A%2F%2Fdl.acm.org%2Fshibboleth

## 选择哪种WAYFless URL 建议遵循以下规则：
### 优先选择标准格式的SP-side WAYFless URL
### 其次选择非标准的SP-side WAYFless URL
### 最后考虑IdP-side WAYFless URL

# WAYFless Shibboleth URL List
## ACM
    https://dl.acm.org/action/ssostart?idp=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&redirectUri=%2F
## ACS
    https://pubs.acs.org/action/ssostart?idp=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&redirectUri=https%3A%2F%2Fpubs.acs.org
## AIP    
    https://iam.atypon.com/action/ssostart?idp=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&redirectUri=%2F&targetSP=https%3A%2F%2Faip.scitation.org
## Annual Reviews
    https://www.annualreviews.org/action/ssostart?idp=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&redirectUri=%2F
## Brill电子书刊平台(博睿)
    https://brill.com/saml/login?idp=https://{IDP地址}/idp/shibboleth
## BrillOnline（博睿学术资源在线平台）
    https://shibboleth2sp.brillonline.nl/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fshibboleth2sp.brillonline.nl%2Fshib%3Fdest%3Dhttps%253A%252F%252Freferenceworks.brillonline.com%253A443%252FSHIBBOLETH%253Fdest%253Dhttps%25253A%25252F%25252Freferenceworks.brillonline.com
## CNKI
    https://fsso.cnki.net/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https://fsso.cnki.net/secure/default.aspx
## Cambridge
注意，两种方式有时候认证通过后仍然会出现选择机构的界面，目前数据库商反馈说短时间内无法解决。
### 方式1（官方提供）
    https://www.cambridge.org/core/idp/{customer ID}
    customer ID 需要向 Cambridge 获取
### 方式2
    https://shibboleth.cambridge.org/Shibboleth.sso/discovery?entityID=https://{IDP地址}/idp/shibboleth&target=https://shibboleth.cambridge.org/CJOShibb2/index?app=https://www.cambridge.org/core/shibboleth
## ClinicalKey
    https://auth.elsevier.com/ShibAuth/institutionLogin?appReturnURL=https%3A%2F%2Fwww.clinicalkey.com%2Fshibboleth%2F&entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth
## De Gruyter
    https://www.degruyter.com/applib/openathens?entityID=https://{IDP地址}/idp/shibboleth&openAthens2Redirect=https%3A%2F%2Fwww.degruyter.com
## EBSCO
### 方式1
    https://shibboleth.ebscohost.com/Shibboleth.sso/Login?SAMLDS=1&target=https%3A%2F%2Fshibboleth.ebscohost.com%2FShibAgent.aspx%3Fshib_returl%3Dhttps%253a%252f%252fsearch.ebscohost.com%252flogin.aspx%253fauthtype%253dshib%26IdpId%3D&entityID=https://{IDP地址}/idp/shibboleth&providerID=http://shibboleth.ebscohost.com
### 方式2(官方提供)
    http://search.ebscohost.com/login.aspx?authtype=ip,shib&custid={customer ID} 
    Customer ID 需要向EBSCO获取
## Embase
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=http%3A%2F%2Fwww.embase.com%2Fcustomer%2Fauthenticate%3Fauth_type%3DSHIBBOLETH
## Emerald Management
    https://www.emerald.com/start-session?idp=https://{IDP地址}/idp/shibboleth
## Engineering Village
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=https%3A%2F%2Fwww.engineeringvillage.com%2Fsearch%2Fquick.url
## Heinonline
    https://heinonline.org/HOL/oa/login?entityID=https://{IDP地址}/idp/shibboleth
## IEEE/IET ELECTRONIC LIBRARY（IEL）
    https://ieeexplore.ieee.org/servlet/wayf.jsp?entityId=https://{IDP地址}/idp/shibboleth&url=https%3A%2F%2Fieeexplore.ieee.org
## IOP Journals
    https://myiopscience.iop.org/signin?origin=deeplink&entity=https://{IDP地址}/idp/shibboleth&target=https://iopscience.iop.org/
## Iresearchbook（爱学术）
    https://spoauth2.carsi.edu.cn/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fspoauth2.carsi.edu.cn%2Fapi%2Fauthorize%3Fresponse_type%3Dcode%26client_id%3Diresearch%26state%3Dcarisi-sp
## Itextbook（爱教材）
    https://spoauth2.carsi.edu.cn/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fspoauth2.carsi.edu.cn%2Fapi%2Fauthorize%3Fresponse_type%3Dcode%26client_id%3Ditext%26state%3Dajc
## JoVE
    https://www.jove.com/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fwww.jove.com%2Fshibboleth%2Fwayf_login.php%3Freturn_page=http://www.jove.com/
## Jstor
    https://shibbolethsp.jstor.org/start?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&site=jstor&dest=%2F
## Keledge（可知）
    https://spoauth2.carsi.edu.cn/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fspoauth2.carsi.edu.cn%2Fapi%2Fauthorize%3Fresponse_type%3Dcode%26client_id%3Dkeledge%26state%3DCARSI
## MeTeL教学资源平台
    https://shibboleth.guodao.cn/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth
## Nature
    https://sp.nature.com/saml/login?idp=https://{IDP地址}/idp/shibboleth&targetUrl=https://www.nature.com/nature
## OSA
    https://osapublishing.org/openathens.cfm?entity=https://{IDP地址}/idp/shibboleth
## OVID
    https://openathens.ovid.com/secure-ssl/home.oa?idpselect=https://{IDP地址}/idp/shibboleth&entityID=https://{IDP地址}/idp/shibboleth&T=JS&CSC=y&PAGE=dblist&NEW
## Oxford English Dictionary Online
    https://shibboleth2sp.sams.oup.com/Shibboleth.sso/Login?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&target=https%3A%2F%2Fshibboleth2sp.sams.oup.com/shib%3Fdest=https://www.oed.com//SHIBBOLETH?dest=%2F
## Oxford Journals Collection
    https://shibboleth2sp.sams2.oup.com/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https://shibboleth2sp.sams2.oup.com/shib?dest=https%3A%2F%2Facademic.oup.com%2FSHIBBOLETH%3Fdest%3D%252Fjournals%252F
## Oxford Reference Library
    https://shibboleth2sp.sams.oup.com/Shibboleth.sso/Login?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&target=https%3A%2F%2Fshibboleth2sp.sams.oup.com/shib%3Fdest=http://www.oxfordreference.com/SHIBBOLETH?dest=%2F
## Oxford Scholarship Online(牛津学术专著电子书)
    https://spoauth2.carsi.edu.cn/Shibboleth.sso/Login?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&target=https%3A%2F%2Fspoauth2.carsi.edu.cn%2Fapi%2Fauthorize%3Fresponse_type%3Dcode%26client_id%3Diresearch%26state%3Dcarisi-sp
## PQDT
    https://spoauth2.carsi.edu.cn/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fspoauth2.carsi.edu.cn%2Fapi%2Fauthorize%3Fresponse_type%3Dcode%26client_id%3Dpqdt%26state%3D1234
## Project Euclid
    https://projecteuclid.org/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https://projecteuclid.org/
## ProjectGate(全球科研项目数据库)
    https://spoauth2.carsi.edu.cn/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fspoauth2.carsi.edu.cn%2Fapi%2Fauthorize%3Fresponse_type%3Dcode%26client_id%3Dprojectgate%26state%3DCASWIZ
## ProQuest
### 方式1
    https://shibboleth-sp.prod.proquest.com/Shibboleth.sso/DS?SAMLDS=1&target=https%3A%2F%2Fshibboleth-sp.prod.proquest.com%2FONE_SEARCH%2FPROD&entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth
### 方式2(官方提供)
    https://search.proquest.com/?accountid={account ID}
    account ID 需要向ProQuest获取
## Reaxys
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https://{IDP地址}/idp/shibboleth&appReturnURL=https%3A%2F%2Fwww.reaxys.com%2Fservices%2Foauth%2Fshibboleth-sso
## RESSET
    https://spoauth2.carsi.edu.cn/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fspoauth2.carsi.edu.cn%2Fapi%2Fauthorize%3Fresponse_type%3Dcode%26client_id%3Dressetdb%26state%3Dyyy
## Royal Society of Chemistry
    https://www.rsc.org/rsc-id/account/checkfederatedaccess?instituteurl=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&returnurl=https%3A%2F%2Fpubs.rsc.org
## ScienceDirect
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=https%3A%2F%2Fwww.sciencedirect.com%2Fuser%2Frouter%2Fshib%3FtargetURL%3Dhttps%253A%252F%252Fwww.sciencedirect.com%252F
## Scival
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=http%3A%2F%2Fwww.scival.com%2F
## Scopus
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=https%3A%2F%2Fwww.scopus.com%2F
## SIAM（Society for Industrial and Applied Mathematics）
    https://epubs.siam.org/action/ssostart?idp=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&redirectUri=/
## Springer Link
    https://fsso.springer.com/federation/init?entityId=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&returnUrl=https%3A%2F%2Flink.springer.com%2F
## Springer Materials
    https://fsso.springer.com/federation/init?entityId=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&returnUrl=https%3A%2F%2Fmaterials.springer.com%2F
## Taylor & Francis E-books 
    https://www.taylorfrancis.com/start-session?idp=https://{IDP地址}/idp/shibboleth&redirectUri=https://www.taylorfrancis.com/
## Taylor & Francis Journals
    http://www.tandfonline.com/action/ssostart?idp=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&redirectUri=https%3A%2F%2Fwww.tandfonline.com%2F
## University Press Scholarship Online (UPSO)    
    https://shibboleth2sp.sams.oup.com/Shibboleth.sso/Login?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&target=https%3A%2F%2Fshibboleth2sp.sams.oup.com/shib%3Fdest=https://www.universitypressscholarship.com/SHIBBOLETH?dest=%2F
## Web of Science
    https://www.webofknowledge.com/?auth=ShibbolethIdPForm&entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&target=https%253A%252F%252Fwww.webofknowledge.com%252F%253FDestApp%253DUA&ShibFederation=ChineseFederation&DestApp=UA
## Wiley
    https://onlinelibrary.wiley.com/action/ssostart?idp=https://{IDP地址}/idp/shibboleth&redirectUri=https://onlinelibrary.wiley.com/
## 万方
    https://shibboleth.wanfangdata.com.cn/Shibboleth.sso/Login?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&target=https%3A%2F%2Fshibboleth.wanfangdata.com.cn%2F
## 重庆维普
    http://qikan.cqvip.com/qikan/carsi/Authorize?entityid=https://{IDP地址}/idp/shibboleth
## 人大复印报刊资料
    https://spoauth2.carsi.edu.cn/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fspoauth2.carsi.edu.cn%2Fapi%2Fauthorize%3Fresponse_type%3Dcode%26client_id%3Drdfybk%26state%3Dpubrudmc
## 易阅通
    https://www.cnpereading.com/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fwww.cnpereading.com%2Fsecure
## 中华数字书苑（方正阿帕比）
    https://spoauth2.carsi.edu.cn/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https%3A%2F%2Fspoauth2.carsi.edu.cn%2Fapi%2Fauthorize%3Fresponse_type%3Dcode%26client_id%3Dapabi%26state%3Dgxjc    
