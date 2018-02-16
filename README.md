# PRLoginRedes


# Cria a estrutura do projeto
dotnet new mvc --auth Individual -o PRLoginRedes

#Configurar o appsettings.json com o código:
{
    "Logging": {
        "IncludeScopes": false,
        "LogLevel": {
            "Default": "Debug",
            "System": "Information",
            "Microsoft": "Information"
        }
    },
    "ConnectionStrings": {
        "DefaultConnection": "data source=.\\sqlexpress; initial catalog=NOMEdoBANCO; user id=USUARIO; password=SENHA"
    },
    "Authentication" : {
        "Facebook": {
            "AppId" : "COLE O APPID AQUI",
            "AppSecret" : "COLE O APPSECRET AQUI"
        },
        "Google" : {
            "ClientId":"COLE O CLIENTID AQUI",
            "project_id":"NOME DO PROJETO",
            "auth_uri":"https://accounts.google.com/o/oauth2/auth",
            "token_uri":"https://accounts.google.com/o/oauth2/token",
            "auth_provider_x509_cert_url":"https://www.googleapis.com/oauth2/v1/certs",
            "ClientSecret":"COLE O CLIENTSECRET AQUI",
            "redirect_uris":["http://localhost:5000/signin-google"],
            "javascript_origins":["http://localhost:5000"]
        },
        "Twitter" : {
            "ConsumerKey" : "COLE A CONSUMERKEY AQUI",
            "ConsumerSecret" : "COLE O CONSUMERSECRET AQUI"
        },
        "Microsoft" : {
            "ApplicationId" : "COLE O APPLICATION ID AQUI",
            "Password" : "COLE O PASSWORD AQUI"
        }
    }
}

#Crie o banco de dados
dotnet ef database update

