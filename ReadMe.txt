steps:-

start local project E:\Official WorkSpace\Intelij_Workspace\Oauth2\ResourceServer on 9090 port and KeyClock [G:\keycloak-26.4.6\bin] on 9091 port by kc.bat start-dev --http-port=9091
http://localhost:9091hit below url and get code value

http://localhost:9091/realms/devrealm/protocol/openid-connect/auth?client_id=IDXXX000&response_type=code&scope=openid profile&redirect_uri=http://localhost:8083/callback&state=awsdadadwe

GetAuthorizationCode- GET request helps to get the AuthorizationCode which we exchange in next POST request to get accessToken
GetAccessToken- in this POST request pass code which we get in previous code, client_secret and redirect_uri [http://localhost:8083/callback] from KeyClock server and we get accessToken and RefreshToken.
