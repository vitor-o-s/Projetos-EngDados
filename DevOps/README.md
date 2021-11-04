# YAML Pipelines and others stuffs related with DevOps

* [SonarQube Pipeline](https://github.com/vitor-o-s/Projetos-EngDados/blob/main/DevOps/sonarqube.yml): This pipelines run code quality analysis using SonarQube, after it's checked if the code has quality to publish, if don't have quality the code isn't posted
* [Deploy](): With this pipeline you can publish on Azure Cloud your Azure function (if you wanna see my example click [here]()). There are two azure functions being published in three Resources Groups (Dev, Qas and Prd), in this pipeline we use azure keyvault to mantain secrets, and library from azure devops to keep the values to appSettings.
