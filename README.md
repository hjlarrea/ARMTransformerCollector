# ARMTransformerCollector

This is a quick view on how the different JSON files will interact. For further information refer to the website (post on my blog) which describes this pattern in depth:

![img](/docs/img01.png)

## How to deploy

### az cli

```bash
az group deployment create -g testDeployment --template-uri https://raw.githubusercontent.com/hjlarrea/ARMTransformerCollector/master/callingTemplate.json --parameters callingTemplate.parameters.json
```

### PowerShell

```powershell
 New-AzureRmResourceGroupDeployment -ResourceGroupName testDeployment -TemplateParameterFile .\callingTemplate.parameters.json -TemplateUri https://raw.githubusercontent.com/hjlarrea/ARMTransformerCollector/master/callingTemplate.json
```