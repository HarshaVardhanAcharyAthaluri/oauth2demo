# oauth2demo

uaac client add webappclient -s webappclientsecret --name WebAppClient --scope resource.read,resource.write,openid,profile,email,address,phone --authorized_grant_types authorization_code,refresh_token,client_credentials,password --authorities uaa.resource --redirect_uri http://localhost:8081/login/oauth2/code/uaa


uaac user add appuser -p appusersecret --emails appuser@acme.com

uaac group add resource.read
uaac group add resource.write

uaac member add resource.read appuser
uaac member add resource.write appuser


client: webappclient
client secret: webappclientsecret

User:appuser
Password:appusersecret
