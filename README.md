# PRLoginRedes


# Cria a estrutura do projeto
dotnet new mvc --auth Individual -o PRLoginRedes

#Configurar o appsettings.json com o código:
{
  "ConnectionStrings": {
    "DefaultConnection": "data source=.\\sqlexpress; initial catalog=NOMEdoBANCO; user id =USUARIO; password=SENHA"
  },
  "Authentication" : {
    "Facebook": {
      //Substituir os dados abaixo
      "AppId" : "APP ID DA APLICAÇÃO",
      "AppSecret" : "CHAVE APPSECRET"
    }
  },
  "Logging": {
    "IncludeScopes": false,
    "LogLevel": {
      "Default": "Warning"
    }
  }
}

