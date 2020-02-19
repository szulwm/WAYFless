# WAYFless

&emsp;&emsp;WAYFless 是一种通过将IDP地址组合在 URL中，避免读者在采用Shibboleth认证时必须先选择自己所在机构的方法，省去了不同 SP界面 各不相同的复杂认证步骤。

&emsp;&emsp;目前支持Shibboleth的数据库中提供WAYFless Shibboleth URL的(使用时，请把URL中的“{IDP地址}”替换为本校的IDP地址，比如idp.xxx.edu.cn)如下所示。

&emsp;&emsp;加入CARSI联盟的各个学校均可使用此方式，方便读者使用。

&emsp;&emsp;本词条由深圳大学图书馆、香港中文大学(深圳)图书馆、清华大学图书馆共同维护。

# WAYFless Shibboleth URL List
## EBSCO
    https://shibboleth.ebscohost.com/Shibboleth.sso/Login?SAMLDS=1&target=https%3A%2F%2Fshibboleth.ebscohost.com%2FShibAgent.aspx%3Fshib_returl%3Dhttps%253a%252f%252fsearch.ebscohost.com%252flogin.aspx%253fauthtype%253dshib%26IdpId%3D&entityID=https://{IDP地址}/idp/shibboleth&providerID=http://shibboleth.ebscohost.com
## ProQuest
    https://shibboleth-sp.prod.proquest.com/Shibboleth.sso/DS?SAMLDS=1&target=https%3A%2F%2Fshibboleth-sp.prod.proquest.com%2FONE_SEARCH%2FPROD&entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth
## IEEE/IET ELECTRONIC LIBRARY（IEL）
    https://ieeexplore.ieee.org/servlet/wayf.jsp?entityId=https://{IDP地址}/idp/shibboleth&url=https%3A%2F%2Fieeexplore.ieee.org
## IOP Journals
    https://connect.openathens.net/saml/2/auth?r=https%3A%2F%2Fconnect.openathens.net/oidc%2Fauth%3Fclient_id%3Diop.com.oidc-app-v1.23cd4589-e9c2-4a1d-8038-de6b5c1a227b%26scope%3Dopenid%26response_type%3Dcode%26redirect_uri%3Dhttps://myiopscience.iop.org/callback?origin=oa&d=iop.com&c=9579783d-3111-430f-8c21-8a2e9ab8096e&as=development&entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth
## Nature
    https://sp.nature.com/saml/login?idp=https://{IDP地址}/idp/shibboleth&targetUrl=https://www.nature.com/nature
## Royal Society of Chemistry
    https://www.rsc.org/rsc-id/account/checkfederatedaccess?instituteurl=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&returnurl=https%3A%2F%2Fpubs.rsc.org
## ScienceDirect
    https://auth.elsevier.com/ShibAuth/institutionLogin?entityID=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&appReturnURL=https%3A%2F%2Fwww.sciencedirect.com%2Fuser%2Frouter%2Fshib%3FtargetURL%3Dhttps%253A%252F%252Fwww.sciencedirect.com%252F
## Springer Link
    https://fsso.springer.com/federation/init?entityId=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&returnUrl=https%3A%2F%2Flink.springer.com%2F
## SpringerMaterials
    https://fsso.springer.com/federation/init?entityId=https%3A%2F%2F{IDP地址}%2Fidp%2Fshibboleth&returnUrl=https%3A%2F%2Fmaterials.springer.com%2F
## CNKI
    https://fsso.cnki.net/Shibboleth.sso/Login?entityID=https://{IDP地址}/idp/shibboleth&target=https://fsso.cnki.net/secure/default.aspx
