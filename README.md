# ARMTransformerCollector

This is a quick view on how the different JSON files will interact. For further information refer to the website (post on my blog) which describes this pattern in depth:

![img](/docs/img01.png)

## How to deploy

### az cli

```bash
git clone https://github.com/hjlarrea/ARMTransformerCollector.git
cd ARMTransformerCollector
az group create --location eastus --name testDeployment
az group deployment create -g testDeployment --template-uri https://raw.githubusercontent.com/hjlarrea/ARMTransformerCollector/master/callingTemplate.json --parameters callingTemplate.parameters.json
```

### PowerShell

```powershell
git clone https://github.com/hjlarrea/ARMTransformerCollector.git
cd ARMTransformerCollector
New-AzureRmResourceGroup -Name testDeployment -Location eastus
New-AzureRmResourceGroupDeployment -ResourceGroupName testDeployment -TemplateParameterFile .\callingTemplate.parameters.json -TemplateUri https://raw.githubusercontent.com/hjlarrea/ARMTransformerCollector/master/callingTemplate.json
```